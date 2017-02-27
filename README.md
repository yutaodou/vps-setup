### Goal

Basic setup for a brand new VPS.

This ansible playbook perform the following operations:

- Install epel-release repo and update 
- Create new user/group with sudo enabled
- Disable password authentication and enable ssh login
- Install shadowsocks and run with supervisord

### How to use
1. Install ansible
2. Update inventory and provide the requested information. 

    See the ansible [FAQ](http://docs.ansible.com/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module) for how to generate encrpted password for the new user.

3. Run the ansible playbook

```
ansible-playbook -i inventory myvps.yml --user root --ask-pass
```