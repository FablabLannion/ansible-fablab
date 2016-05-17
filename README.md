

# ansible-fablab
Ansible playbook for our server


## Usage

* set password file base on template (use ansible-vault: http://docs.ansible.com/ansible/playbooks_vault.html)

```
cd vars
cp fablab-password.yml.tpl fablab-password.yml
ansible-vault encrypt fablab-password.yml
ansible-vault edit fablab-password.yml
```

* Run

First go back to root of the project. Then:

```
ansible-playbook -i production --ask-vault-pass fablab.yml
```

## Sources

Somes roles used by the playbook are cloned and modified from other projects:

* wordpress: https://github.com/darthwade/ansible-role-wordpress [MIT]
* apache: https://github.com/geerlingguy/ansible-role-apache [MIT]
* letsencrypt: https://github.com/thefinn93/ansible-letsencrypt  
* openldap_server: https://github.com/bennojoy/openldap_server [BSD]

## License

Apache 2
