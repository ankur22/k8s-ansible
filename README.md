Credentials File
You will need to create an encrypted vault file which contains:

```
cluster_username: username
cluster_password: password
cluster_sudo_password: sudo_password
```

Apt Update and Upgrade

```
ansible-playbook -i all-hosts update.yaml --vault-password-file ansible-vault-password --extra-vars '@vault.yaml'
```

