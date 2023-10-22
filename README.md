# [openssh-server-gael](https://snapcraft.io/openssh-server-gael)

_This is NOT an original piece of work, just a snap of OpenSSH server_

The SSH2 protocol implemented in OpenSSH is standardized by the IETF secsh working group and is specified in several RFCs and drafts. The overall structure of SSH2 is described in the architecture RFC.

**Installation**

`sudo snap install openssh-server-gael_8.9_amd64.snap --devmode`

**First use**

* Read the doc at https://man.openbsd.org/sshd on how to get started.

* Create a SSH host key
`sudo openssh-server-gael.ssh-keygen -t ed25519 -f /var/snap/openssh-server-gael/current/ssh_host_ed25519_key`

* Configure the server
`sudo vi /var/snap/openssh-server-gael/current/sshd_config`

* Start and enable OpenSSH server
`sudo snap start --enable openssh-server-gael.sshd`

* Read the logs
`sudo snap logs -n 30 openssh-server-gael.sshd`

**2023-08-08**

* First build
