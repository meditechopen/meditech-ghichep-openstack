## Các tài liệu về OpenStack

### Cấu trúc thư mục:

- `docs`: Nơi lưu trữ những bài viết về cài đặt, vận hành Openstack
- `images`: Nơi lưu trữ các hình ảnh phục vụ cho các bài viết
- `tools`: Nơi lưu trữ source code của openstack được tải từ trang chủ
- `script`: Lưu trữ các script tự động cài đặt openstack và một số plugin nhóm tự viết

### Nội dung

#### Cài đặt

- [1. Hướng dẫn cài đặt OpenStack Newton bằng Packstack trên CentOS 7](./docs/00.Setup-OpenStack/packstack.md)
- [2. Hướng dẫn cài đặt OpenStack Newton trên CentOS 7 sử dụng Linux Bridge](/docs/00.Setup-OpenStack/hd-caidat-openstack-newton-centos7.md)
- [3. Hướng dẫn cài đặt OpenStack Newton trên CentOS 7 sử dụng OVS và Bonding](./docs/00.Setup-OpenStack/hd-caidat-openstack-newton-OVS-bonding.md)

## Keystone

### Ghi chép keystone

- [Tổng quan keystone](./docs/01.Keystone/Fundamental-keystone.md)
- [Giải thích file cấu hình cơ bản](./docs/01.Keystone/configuration-file.md)
- [Các lệnh cơ bản trong Keystone](./docs/01.Keystone/cli-keystone.md)
- [Giải thích về token trong keystone](./docs/01.Keystone/token-format.md)

### Lab với keystone

- [Lab keystone cơ bản](./docs/01.Keystone/using-keystone.md)
- [File policy.json và định nghĩa một role](./docs/01.Keystone/file-policy.json.md)

## Glance

### Ghi chép Glance

- [Tổng quan glance](./docs/02.Glance/glance-overview.md)
- [Giải thích file cấu hình cơ bản](./docs/02.Glance/file-config-glance.md)
- [Các lệnh cơ bản trong Glance](./docs/02.Glance/cli-glance.md)

### Lab với glance

- [Lab glance cơ bản](./docs/02.Glance/manage-glance.md)

## Neutron

### Ghi chép Neutron

- [Tổng quan neutron](./docs/04.Neutron/OpenStack-Networking-basic.md)
- [Tổng quan OpenvSwitch](./docs/04.Neutron/openvswitch.md)
- [Tổng quan bonding](./docs/Neutron/bonding.md)
- [Kiến trúc và traffic flow trong neutron](./docs/04.Neutron/neutron-openvswitch.md)
- [Các lệnh cơ bản trong Neutron](./docs/04.Neutron/cli-neutron.md)
- [Giải thích file cấu hình cơ bản](./docs/04.Neutron/file-config.md)

### Lab với neutron

- [Lab neutron cơ bản](./docs/04.Neutron/manage-neutron.md)

## Nova

### Ghi chép nova

- [Tổng quan nova](./docs/03.Nova/nova-overview.md)
- [Giải thích file cấu hình cơ bản](./docs/03.Nova/file-config-nova.md)
- [Workflow tạo máy ảo trong nova](./docs/03.Nova/request-flow-for-provisioning-instance.md)
- [Giải thích cơ chế filter và weight của nova-schedule](./docs/03.Nova/nova-scheduler.md)
- [Các lệnh cơ bản trong Nova](./docs/03.Nova/cli-nova.md)

### Lab với nova

- [Lab nova cơ bản](./docs/03.Nova/manage-nova.md)

## Cinder

### Ghi chép cinder

-	[Tổng quan về Cinder](./docs/05.Cinder/tongquan-cinder.md)
-	[Cinder WorkFlow](./docs/Cinder/05.cinder-workflow.md)
-	[Giải thích file cấu hình Cinder](./docs/05.Cinder/cinder-config-explain.md)
- [Cơ chế filter và weight của cinder-scheduler](./docs/05.Cinder/cinder-scheduler.md)
- [Các lệnh cơ bản trong Cinder](./docs/05.Cinder/cinder-cli.md)

### Lab với cinder

-	[Cài đặt Cinder](./docs/05.Cinder/OPS-cinder.md)
-	[Câu lệnh với Cinder](./docs/05.Cinder/cinder-cli.md)
-	[Cinder với backend là GlusterFS](./docs/05.Cinder/cinder-glusterfs.md)
- [Hướng dẫn cấu hình multiple Cinder và thực hiện tính năng migrate volume](./docs/05.Cinder/cinder.md)

## Metadata

- [Tìm hiểu về metadata service](./docs/06.Metadata/metadata.md)
- [Tìm hiểu về cloud-init](./docs/06.Metadata/cloud-init-intro.md)
- [Một số ví dụ với cloud-config](./docs/06.Metadata/examples.md)
- [Một số module phổ biến thường được dùng trong cloud-init](./docs/06.Metadata/module.md)

## Một số functions

- [Hướng dẫn rebuild lại máy ảo trong trường hợp Compute bị chết](./docs/07.Functions/evacuate.md)
- [Tìm hiểu về migrate máy ảo trong OpenStack](./docs/07.Functions/migration.md)
- [Hướng dẫn resize máy ảo](./docs/07.Functions/resize.md)
- [Hướng dẫn reset root password của máy ảo CentOS 7 trên OpenStack](./docs/07.Functions/Huong-dan-reset-root-password-may-ao-centos-tren-openstack.md)

## Hướng dẫn tạo image

- [Hướng dẫn đóng image CentOS 7 với Cloud-init (không dùng LVM)](./docs/08.Image-create/CentOS-7-cloudinit-noLVM.md)
- [Hướng dẫn đóng image Ubuntu 14.04 với cloud-init (không dùng LVM)](./docs/08.Image-create/Ubuntu14-04-cloudinit-noLVM.md)

(C) MediTech JSC,. - https://meditech.vn
