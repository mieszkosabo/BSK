# BSK

## Setting up ssh on debian 10
1. VirtualBox settings -> Network -> Bridged Adapter
2. `$ sudo apt-get install openssh-server`
3. `$ sudo systemctl enable ssh`
3. `vim /etc/ssh/sshd_config` and change `#PermitRootLogin <sth>` to `PermitRootLogin yes`
4. `# /etc/init.d/ssh restart`
5. check your ip: `ifconfig`
6. from host machine: `ssh root@<ip_from_step_5>`
7. (optional) omit entering password when ssh'ing from host to remote: `ssh-copy-id -i ~/.ssh/id_rsa.pub remote-host`

## groups and users
[how to manage users and groups](https://www.linux.com/topic/desktop/how-manage-users-groups-linux/)
