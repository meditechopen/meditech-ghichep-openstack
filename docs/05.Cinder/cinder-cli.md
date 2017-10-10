# Các câu lệnh hay dùng với Cinder (Đối với Cinder sử dụng LVM làm storage backend)

# Mục lục

 *	[1 Tạo volume bằng câu lệnh](#1)
	*	[1.1 Tạo Bootable-Volume và tạo máy ảo từ bootable-volume](#1.2)
	*	[1.1 Tạo non-bootable volume, thực hiện gắn và gõ khỏi máy ảo](#1.3)
 *	[2 Resize volume](#2)
 *	[3 Volume Snapshot](#3)



## 1. Tạo volume bằng câu lệnh <a name="1"> </a>

Trong Openstack, volume được chia thành 2 dạng :

	- Volume dùng để boot máy ảo (bootable volume)
	- Volume dùng để gắn vào máy ảo, dùng như một ổ đĩa ngoài (non-booable volume)

### 1.1 Tạo Bootable-Volume và tạo máy ảo từ bootable-volume <a name="1.1"> </a>

 - Trước khi tạo bootable-volume, cần có các thông tin sau :
	- --flavor=ID
	- --image=ID
	- --nic net-id=ID
	- --block-device source=volume,id=ID,dest=DEST,size=SIZE,shutdown={preserve|remove},bootindex=0

 - Kiểm tra các thông tin trên với câu lệnh

```sh
openstack flavor list
openstack image list
openstack network list
```

 - Tạo máy ảo với các thông tin đã có

`nova boot --flavor m1.tiny --nic net-id=e658e30c-af97-4d77-98a3-bf9b6776c25e --block-device source=image,id=785b8fe0-e5fd-4533-b56f-a5ac1014bf6c,dest=volume,size=10,shutdown=preserve,bootindex=0 vm-01`

 - Liệt kê các máy ảo được tạo

`openstack server list`

 - Show ra thông tin chi tiết máy ảo đã tạo

`openstack server show VM-Name/VM-ID`


### 1.2 Tạo non-bootable volume, thực hiện gắn và gõ khỏi máy ảo. <a name="1.2"> </a>

Các bước dưới đây để kiểm chứng việc dữ liệu trên non-bootable volume sẽ không bị mất khi gắn volume từ máy ảo này sang máy ảo khác.

**Chú ý** : Thực hiện trên node Controller

#### 1.2.1 Tạo non-bootable volume <a name="1.2.1"> </a>

	- Cú pháp

`cinder create --display-name VOLUME-NAME VOLUME-SIZE --volume-type VOLUME_TYPE  `

	- Ví dụ

`cinder create --display-name vl1 10`

![cinder1](/images/volume-create.png)


**Chú ý** : Tham khảo link [sau](https://docs.openstack.org/admin-guide/dashboard-manage-volumes.html) để tạo volume_type

#### 1.2.2 List ra các volume đã có <a name="1.2.2"> </a>

`cinder list`

![cinder1](/images/cinder-list.png)

#### 1.2.3 Attach non-bootable volume vào vm

 - Gán volume trạng thái **Available** vào máy ảo như một ổ cứng bên ngoài

	- Cú pháp
	`openstack server add volume --device /dev/vdd	ten-vm ten-volume`

	- Ví dụ
	`openstack server add volume  vm-01 lv-01`

 - Ta sẽ attach non-bootable volume vào vm-01 , cóp dữ liệu vào volume.

	- Tại vm được gắn volume, thực hiện format ổ cứng, mount thư mục và đẩy dữ liệu vào volume

```sh
mkfs -t ext4 /dev/vdd
mkdir -p /test/
mount /dev/vdd /test/
echo "MeditechJSC" > /test/meditech.txt
```
	- Xem nội dung có trong file

`cat /test/meditech.txt`

```sh
MeditechJSC
```

#### 1.2.4 Detech volume ra khỏi vm

 - Thực hiện umount, detach volume khỏi máy ảo cũ.

```sh
umount /dev/vdd /test/
openstack server remove volume  vm-01 lv-01
```

 - Trên máy ảo mới, tạo thư mục, mount volume.

```sh
mkdir -p /test/
mount /dev/vdd /test/
```

 - Kiểm tra dữ liệu trong volume

`cat /test/meditech.txt`

```sh
MeditechJSC
```

### 2 Resize volume <a name="2"> </a>

 - Để resize volume, detach volume khỏi server, sau đó resize volume

`cinder extend VOLUME-NAME SIZE`

 - Kiểm tra lại trạng thái volume

`cinder list`

### 3 Volume Snapshot <a name="3"> </a>

Volume snapshot chụp một thời điểm trạng thái của volume. Volume mà có snapshot được tạo từ nó sẽ không thẻ xóa nếu các snapshot vẫn còn tồn tại. Volume phải ở trạng thái **unattach** để có thể tạo snapshot. Để dùng snapshot, một volume mới phải được từ snapshot.

Volume snapshot khác với volume backup. Backup copy taofn bộ volume được lưu trữ trong Object Storage trong khi snapshot chỉ giống như một bức ảnh chụp một thời điểm của volume. Volume backup hoàn toàn độc lập với volume nguyên bản.

 - Kiểm tra trạng thái volume

`cinder list`


|                  ID                  |   Status  |    Name   | Size | Volume Type | Bootable | Attached to |
|--------------------------------------|-----------|-----------|------|-------------|----------|-------------|
| 6742baf4-3ae6-41e2-b7bc-fddaeb385370 | available | my-volume |  10  |     lvm     |  false   |             |


 - Tạo snapshot từ volume

`cinder snapshot-create my-volume --name snap1`


|   Property  |                Value                 |
|-------------|--------------------------------------|
|  created_at |      2017-04-05T04:38:04.308547      |
| description |                 None                 |
|      id     | 1be3814f-ecd2-4010-86c6-040b2ef15fa4 |
|   metadata  |                  {}                  |
|     name    |                snap1                 |
|     size    |                  10                  |
|    status   |               creating               |
|  updated_at |                 None                 |
|  volume_id  | 6742baf4-3ae6-41e2-b7bc-fddaeb385370 |


 - Kiểm tra trạng thái các snapshot đã tạo

`cinder snapshot-list`

|                  ID                  |              Volume ID             |   Status  |  Name | Size |
|--------------------------------------|------------------------------------|-----------|-------|------|
| 1be3814f-ecd2-4010-86c6-040b2ef15fa4 | 6742baf4-3ae6-41e2-b7bc-fddaeb385370 | available | snap1 |  10  |


### 1.5 Migrate Volume

Xem thêm [tại đây](/docs/Cinder/cinder.md)

### 1.6 Volume Backup

Bổ sung sau
