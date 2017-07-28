# Cinder Volume với Backend là GluterFS

# Mục lục

 *	[1 Chuẩn bị](#1)
 *	[2 Chuẩn bị hệ thống GlusterFS](#2)
 *	[3 Cấu hình GlusterFS Backend trên node Cinder](#3)
 *	[4 Cấu hình GlusterFS Backend trên node Compute](#4)
 *	[5 Cấu hình GlusterFS Backend trên node Controller](#5)
 *	[6 Tạo volume và kiểm tra](#6)

## 1 Chuẩn bị <a name="1"> </a>

 - Mô hình Lab

![cinder1](/images/cinder-gluster.png)

 - IP-Planning

![cinder1](/images/ip-plan.png)

## 2 Chuẩn bị hệ thống GlusterFS <a name="2"> </a>

 -	Chuẩn bị 2 máy GlusterFS, tham khảo cài đặt ở link [sau](https://github.com/meditechopen/mdt-technical/blob/master/TRIMQ/GlusterFS/glusterfs.md#33)

 -	Kiểm tra volume được tạo trên 2 máy GlusterFS

`gluster volume status`

![cinder1](/images/gluster-volume-status.png)

**Tham khảo**

 - Câu lệnh xóa volume trên glusterfs

`gluster volume delete volume-name`

## 3 Cấu hình GlusterFS Backend trên node Cinder <a name="3"> </a>

 -	Cài đặt GlusterFS Client

`yum -y install glusterfs glusterfs-fuse`

 -	Chỉnh sửa và thêm trong file `/etc/cinder/cinder.conf`

```sh
[DEFAULT]
enabled_backends = glusterfs

[glusterfs]
volume_driver = cinder.volume.drivers.glusterfs.GlusterfsDriver
glusterfs_shares_config = /etc/cinder/glusterfs_shares
glusterfs_mount_point_base = $state_path/mnt_gluster
```

 -	Tạo file `/etc/cinder/glusterfs_shares` và link tới volume của glusterFS

`vi /etc/cinder/glusterfs_shares`

```sh
172.16.69.13:/cinder-vol
```

 - Khởi động GlusterFS backend

```sh
chmod 640 /etc/cinder/glusterfs_shares
chgrp cinder /etc/cinder/glusterfs_shares
systemctl restart openstack-cinder-volume
```

 -	Kiểm tra Cinder đã mount tới GlusterFS backend

`df -hT`

![cinder1](/images/cinder-mount.png)

## 4 Cấu hình GlusterFS Backend trên node Compute <a name="4"> </a>

 -	Cài đặt GlusterFS Client

`yum -y install glusterfs glusterfs-fuse`

 -	Chỉnh sửa `/etc/nova/nova.conf`

```sh
[DEFAULT]
volume_api_class = nova.volume.cinder.API
```

 -	Restart lại service

`systemctl restart openstack-nova-compute`

## 5 Cấu hình GlusterFS Backend trên node Controller <a name="5"> </a>

 -	Tạo volume-type là glusterfs

`cinder type-create glusterfs`

 -	Kiểm tra volume-type vừa tạo

`cinder type-list`

|                  ID                  |    Name   | Description | Is_Public |
|--------------------------------------|-----------|-------------|-----------|
| 2ec412a2-11f9-4ee9-bcf7-386019fc8b22 | glusterfs |      -      |    True   |

 -	Thêm volume-type vừa tạo vào file cấu hình cinder

`cinder type-key glusterfs set volume_backend_name=GlusterFS`

 -	Kiểm tra cấu hình

`cinder extra-specs-list`

|                  ID                  |    Name   |             extra_specs              |
|--------------------------------------|-----------|--------------------------------------|
| 2ec412a2-11f9-4ee9-bcf7-386019fc8b22 | glusterfs | {'volume_backend_name': 'GlusterFS'} |

 -	Thêm biến trong file admin-rc

`echo "export OS_VOLUME_API_VERSION=2" >> ~/admin-rc`

`source admin-rc`

## 6 Tạo volume và kiểm tra <a name="6"> </a>
 -	Tạo non-bootable volume tới volume-type

`cinder create --display_name disk01 10 --volume-type glusterfs`

 -	Kiểm tra Volume vừa tạo

`cinder list`

|ID|   Status  |    Name   | Size | Volume Type | Bootable |Attached to|
|--|-----------|-----------|------|-------------|----------|-----------|
|706f8901-258b-4435-b75d-247601666b5a| available |disk01|10|glusterfs|false||

 -	Thực hiện kiểm tra volume, tham khảo link [sau](https://github.com/meditechopen/mdt-technical/blob/master/ManhDV/OpenStack/Cinder/docs/thuchanh/cinder-cli.md#1.3) (mục 1.1 Tạo non-bootable volume, thực hiện gắn và gõ khỏi máy ảo)
