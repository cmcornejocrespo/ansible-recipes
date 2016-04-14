This is similar to secrets, but user is not prompted for password.
Password is stored in a file instead. This is useful for automation,
for example running ansible from jenkins.

First we need to set env variable `ANSIBLE_VAULT_PASSWORD_FILE` which
will store path to the file storing passoword.

`ANSIBLE_VAULT_PASSWORD_FILE=pass ansible-playbook main.yml`
