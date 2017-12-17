Ansible Role: vsftpd
=========

Installs and configures the vsftpd FTP server.
Anonymous uploads and downloads can be used at home/office to store
scanned documents from you network connected scanner.  Any web browser can be
used to download the scanned documents.

SELinux contexts and booleans are taken care of in the role.

Requirements
------------

None.

Role Variables
--------------

```
vsftpd_accept_timeout:            20
vsftpd_allow_root_login:          false
vsftpd_allow_writeable_chroot:    YES
vsftpd_anonymous_enable:          YES
vsftpd_anon_max_rate:             0
vsftpd_anon_mkdir_write_enable:   YES
vsftpd_anon_other_write_enable:   YES
vsftpd_anon_upload_enable:        YES
vsftpd_anon_root:                 /var/ftp/pub
vsftpd_anon_umask:                022
vsftpd_anon_world_readable_only:  YES
vsftpd_ascii_upload_enable:       YES
vsftpd_ascii_download_enable:     YES
vsftpd_async_abor_enable:         YES
vsftpd_chroot_local_user:         YES
vsftpd_chroot_list_enable:        YES
vsftpd_chroot_list_file:          /etc/vsftpd/chroot_list
vsftpd_connect_from_port_20:    NO
vsftpd_connect_timeout:           20
vsftpd_data_connection_timeout: 300
vsftpd_ftpd_banner:             Spurrier family only.
vsftpd_hide_ids:                YES
vsftpd_idle_session_timeout:    120
vsftpd_ls_recurse_enable:   NO
vsftpd_listen:                  YES
vsftpd_listen_ipv6:         NO
vsftpd_local_enable:        NO
vsftpd_max_clients:             12
vsftpd_max_per_ip:              3
vsftpd_one_process_model:       YES
vsftpd_pasv_min_port:           6970
vsftpd_pasv_max_port:           6980
vsftpd_seccomp_sandbox:     NO
vsftpd_tcp_wrappers:        NO
vsftpd_userlist_enable:         YES
vsftpd_userlist_deny:           YES
vsftpd_userlist_file:           /etc/vsftpd/user_list
vsftpd_use_localtime:           YES
vsftpd_xferlog_file:            /var/log/vsftpd.log
vsftpd_writable_dirs:
  - '/var/ftp/pub/scans'
vsftpd_write_enable:            YES
```

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: shomatan.vsftpd }

License
-------

MIT

Author Information
------------------

Shoma Nishitateno
