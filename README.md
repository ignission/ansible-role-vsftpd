Ansible Role: vsftpd
=========

Installs secure and fastest FTP server.

Requirements
------------

None.

Role Variables
--------------

    vsftpd_allow_root_login: false

    # vsftpd.conf
    vsftpd_allow_writeable_chroot: YES
    vsftpd_anonymous_enable: NO
    vsftpd_ascii_upload_enable: YES
    vsftpd_ascii_download_enable: YES
    vsftpd_chroot_local_user: YES
    vsftpd_chroot_list_enable: YES
    vsftpd_chroot_list_file: /etc/vsftpd/chroot_list
    vsftpd_ftpd_banner: Welcome to my FTP service.
    vsftpd_ls_recurse_enable: YES
    vsftpd_listen: YES
    vsftpd_listen_ipv6: NO
    vsftpd_seccomp_sandbox: NO
    vsftpd_userlist_enable: YES
    vsftpd_userlist_deny: YES
    vsftpd_userlist_file: /etc/vsftpd/user_list
    vsftpd_use_localtime: YES
    vsftpd_xferlog_file: /var/log/vsftpd.log
    vsftpd_pasv_min_port: 6970
    vsftpd_pasv_max_port: 6980

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