
# About #

Installs qemu on chosen debian hosts, suitable for ansible-based guest provisionning using https://github.com/alemansec/ansible-role-qemu-provision-machine role.

- This role ("ansible-role-qemu-host") also creates directory structures required by "ansible-role-qemu-provision-machine" role,
- downloads configured debian iso files,
- configures basic networking
- generates a default preseed.cfg file

Note that this is amd64-oriented only for now.


# Howto #

Sample is included under ```sample_usage/``` ; i'll soon add a meta-repository (as in 'git submodules') using both roles, which is the point of me publishing those roles at m$^H^Hgithub.com.

- edit defaults/main.yml (ssh keys, default passwords, mirrors, TZ, ...)
- cd sample_usage/
- edit inventory/sample/hosts
- check/edit ansible.cfg accordiningly
- ansible-playbook book_qemu_host.yml

