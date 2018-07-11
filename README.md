# ho-ansible/distcc
Ansible role to configure a distcc server;
i.e., a worker that can be called from a remote compiler.

# Role variables
+ `distcc_listen` (default: localhost): IP to bind to.
  Set to empty string (`""`) to disable server and use ssh to run distcc.
+ `distcc_nets` (default: 127.0.0.0/8): clients in these subnets are allowed
  to connect.
+ `distcc_loglevel` (default: warning): verbosity of distcc log
+ `distcc_nice` (default: 5): priority of compile processes,
  higher nice means lower priority
