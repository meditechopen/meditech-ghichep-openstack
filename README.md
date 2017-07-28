## Các tài liệu về OpenStack

### Cấu trúc thư mục:

- `docs`: Nơi lưu trữ những bài viết về cài đặt, vận hành Openstack
- `images`: Nơi lưu trữ các hình ảnh phục vụ cho các bài viết
- `tools`: Nơi lưu trữ source code của openstack được tải từ trang chủ
- `script`: Lưu trữ các script tự động cài đặt openstack và một số plugin nhóm tự viết

### Nội dung

#### Cài đặt

- [1. Hướng dẫn cài đặt OpenStack Newton bằng Packstack trên CentOS 7](./docs/packstack.md)
- [2. Hướng dẫn cài đặt OpenStack Newton trên CentOS 7 sử dụng Linux Bridge](./docs/hd-caidat-openstack-newton-centos7.md)
- [3. Hướng dẫn cài đặt OpenStack Newton trên CentOS 7 sử dụng OVS và Bonding](./docs/hd-caidat-openstack-newton-OVS-bonding.md)
=======
 - [00. Hướng dẫn cài đặt openstack newton](docs/00.Setup-OpenStack/packstack.md)
 - [01. Keystone](docs/01.Keystone)

## Keystone

### Ghi chép keystone

- [Tổng quan keystone](./docs/Keystone/Fundamental-keystone.md)
- [Giải thích file cấu hình cơ bản](./Keystone/docs/configuration-file.md)
- [Giải thích về token trong keystone](./Keystone/docs/token-format.md)

### Lab với keystone

- [Lab keystone cơ bản](./docs/Keystone/using-keystone.md)
- [File policy.json và định nghĩa một role](./docs/Keystone/file-policy.json.md)

## Glance

### Ghi chép Glance

- [Tổng quan glance](./docs/Glance/glance-overview.md)
- [Giải thích file cấu hình cơ bản](./docs/Glance/file-config-glance.md)

### Lab với glance

- [Lab glance cơ bản](./docs/Glance/manage-glance.md)

## Neutron

### Ghi chép Neutron

- [Tổng quan neutron](./docs/Neutron/OpenStack-Networking-basic.md)
- [Tổng quan OpenvSwitch](./docs/Neutron/openvswitch.md)
- [Tổng quan bonding](./docs/Neutron/bonding.md)
- [Kiến trúc và traffic flow trong neutron](./docs/Neutron/neutron-openvswitch.md)

### Lab với neutron

- Lab neutron cơ bản

## Nova

### Ghi chép nova

- [Tổng quan nova](./docs/Nova/nova-overview.md)
- [Giải thích file cấu hình cơ bản](./docs/Nova/file-config-nova.md)
- [Workflow tạo máy ảo trong nova](./docs/Nova/request-flow-for-provisioning-instance.md)
- [Giải thích cơ chế filter và weight của nova-schedule](./docs/Nova/nova-scheduler.md)

### Lab với nova

- [Lab nova cơ bản](./docs/Nova/manage-nova.md)
- [Migrate máy ảo](./docs/migration.md)
- [Evacuate máy ảo](./docs/evacuate.md)

## Cinder

### Ghi chép cinder

-	[Tổng quan về Cinder](./docs/Cinder/tongquan-cinder.md)
-	[Cinder WorkFlow](./docs/Cinder/cinder-workflow.md)
-	[Giải thích file cấu hình Cinder](./docs/Cinder/cinder-config-explain.md)
- [Cơ chế filter và weight của cinder-scheduler](./docs/Cinder/cinder-scheduler.md)

### Lab với cinder

-	[Cài đặt Cinder](./docs/Cinder/OPS-cinder.md)
-	[Câu lệnh với Cinder](./docs/Cinder/cinder-cli.md)
-	[Cinder với backend là GlusterFS](./docs/Cinder/cinder-glusterfs.md)
- [Hướng dẫn cấu hình multiple Cinder và thực hiện tính năng migrate volume](./docs/Cinder/cinder.md)

(C) MediTech JSC,. - https://meditech.vn
