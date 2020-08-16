# ho-ansible/distcc
Ansible role to configure a distcc server;
i.e., a worker that can be called from a remote compiler.

## DEPRECATED
This ansible role is no longer maintained.

# Role variables
+ `distcc_listen` (default: localhost): IP to bind to in daemon mode.
  Set to empty string (`""`) to disable daemon and run in inetd mode.

## Variables for daemon mode
+ `distcc_nets` (default: 127.0.0.0/8): clients in these subnets are allowed
  to connect to the daemon.
+ `distcc_loglevel` (default: warning): verbosity of distcc log
+ `distcc_nice` (default: 5): priority of compile processes,
  higher nice means lower priority

## Variables for inetd mode
+ `distcc_home` (default: /var/tmp/distcc): homedir of the `distcc_user`
+ `distcc_sshkeys`: SSH public keys to allow login as `distcc_user`
