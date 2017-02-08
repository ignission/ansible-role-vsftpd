# Ansible role: vsftpd

## Requirements
None.

## Role Variables
|Key|Type|Description|Default|
|:--|:---|:----------|:------|
|vsftpd_allow_root_login|boolean||false|
|vsftpd_allow_writeable_chroot|YES,NO||YES|
|vsftpd_anonymous_enable|YES,NO||NO|
|vsftpd_ascii_upload_enable|YES,NO||YES|
|vsftpd_ascii_download_enable|YES,NO||YES|
|vsftpd_chroot_local_user|YES,NO||YES|
|vsftpd_chroot_list_enable|YES,NO||YES|
|vsftpd_chroot_list_file|String||/etc/vsftpd/chroot_list|
|vsftpd_ftpd_banner|String||Welcome to my FTP service.|
|vsftpd_ls_recurse_enable|YES,NO||YES|
|vsftpd_listen|YES,NO||YES|
|vsftpd_listen_ipv6|YES,NO||NO|
|vsftpd_seccomp_sandbox|YES,NO||NO|
|vsftpd_userlist_enable|YES,NO||YES|
|vsftpd_userlist_deny|YES,NO||YES|
|vsftpd_userlist_file|String||/etc/vsftpd/user_list|
|vsftpd_use_localtime|YES,NO||YES|
|vsftpd_xferlog_file|String||/var/log/vsftpd.log|
|vsftpd_pasv_min_port|Integer||6970|
|vsftpd_pasv_max_port|Integer||6980|

## Dependencies
None.

## Example playbook

```yaml
- hosts: all
  roles:
    - role: vsftpd
```
