## Giới hạn mức sử dụng của User và Upload Image

### Menu

- 1. Giới hạn mức sử dụng của user
- 2. Giới hạn size và dung lượng Image của User

### 1. Giới hạn mức sử dụng của user

Trên node `controller`, chúng ta sửa file cấu hình của `nova`:

```
vi /etc/nova/nova.conf
```

```
...
# Number of instances allowed per project (integer value)
quota_instances=10

# Number of instance cores allowed per project (integer value)
quota_cores=5

# Megabytes of instance RAM allowed per project (integer value)
quota_ram=10240

# Number of floating IPs allowed per project (integer value)
quota_floating_ips=15

# Number of fixed IPs allowed per project (this should be at least the number
# of instances allowed) (integer value)
#quota_fixed_ips=-1

# Number of metadata items allowed per instance (integer value)
#quota_metadata_items=128

# Number of injected files allowed (integer value)
#quota_injected_files=5

# Number of bytes allowed per injected file (integer value)
#quota_injected_file_content_bytes=10240

# Length of injected file path (integer value)
#quota_injected_file_path_length=255

# Number of security groups per project (integer value)
#quota_security_groups=10

# Number of security rules per security group (integer value)
#quota_security_group_rules=20

# Number of key pairs per user (integer value)
#quota_key_pairs=100

# Number of server groups per project (integer value)
#quota_server_groups=10

# Number of servers per server group (integer value)
#quota_server_group_members=10
...
```

Sau khi đặt giới hạn xong, chúng ta khởi động lại dịch vụ.

```
systemctl restart openstack-nova*
```

Và kiểm tra lại bằng lệnh:

```
source ~/keystonerc_admin
nova quota-show
```

```sh
[root@controller ~(keystone_admin)]# nova quota-show
+-----------------------------+-------+
| Quota                       | Limit |
+-----------------------------+-------+
| instances                   | 10    |
| cores                       | 5     |
| ram                         | 10240 |
| floating_ips                | 15    |
| fixed_ips                   | -1    |
| metadata_items              | 128   |
| injected_files              | 5     |
| injected_file_content_bytes | 10240 |
| injected_file_path_bytes    | 255   |
| key_pairs                   | 100   |
| security_groups             | 10    |
| security_group_rules        | 20    |
| server_groups               | 10    |
| server_group_members        | 10    |
+-----------------------------+-------+
```

### 2. Giới hạn size và dung lượng Image của User

`Glance` cho phép chúng ta đặt khá nhiều giới hạn về Image. Tuy nhiên, trong bài hướng dẫn này tôi chỉ hướng dẫn các bạn giới hạn dung lượng của file IMAGE và giới hạn dung lượng cho mỗi user.

```
vi /etc/glance/glance-api.conf
```

```
...
# Maximum size of image a user can upload in bytes. Defaults to
# 1099511627776 bytes (1 TB).WARNING: this value should only be
# increased after careful consideration and must be set to a value
# under 8 EB (9223372036854775808). (integer value)
# Maximum value: 9223372036854775808
image_size_cap = 1073741824

# Set a system wide quota for every user. This value is the total
# capacity that a user can use across all storage systems. A value of
# 0 means unlimited.Optional unit can be specified for the value.
# Accepted units are B, KB, MB, GB and TB representing Bytes,
# KiloBytes, MegaBytes, GigaBytes and TeraBytes respectively. If no
# unit is specified then Bytes is assumed. Note that there should not
# be any space between value and unit and units are case sensitive.
# (string value)
user_storage_quota = 2GB
...
```

- **Chú thích**:
	- `image_size_cap =  1073741824`: Dung lượng của file IMAGE. Tính theo byte, ví dụ này là 1GB.
	- `user_storage_quota = 2GB`: Mỗi USER sẽ có 2GB lưu trữ
	
Sau khi đặt giới hạn, chúng ta khởi động lại Glane bằng lệnh:

```
systemctl restart openstack-glance-api
```