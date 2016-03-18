## Example of dealing with secrets.
`ansible.cfg` is configured to ask user for `ansible-vault` password.
`roles/ssh_key/tasks/main.yml` loads variable `id_rsa` from
`roles/ssh_key/vars/main.yml` which is encrypted with `ansible-vault` command
and uses ansible user's home directory to store the key.

To view the encrypted vars file, use `test` password.

If the `copy` module uses `src` attribute instead of `content` and the secret
is stored in a file, the encrypted (instead of decrypted) content would be
copied.
