# K8s-Ansible
This is used to provision the Raspberry Pi nodes in the single cluster.

## Credentials File
You will need to create an encrypted vault file which contains:

```
cluster_username: username
cluster_password: password
cluster_sudo_password: sudo_password
```

## Apt Update and Upgrade

```
ansible-playbook -i all-hosts update.yaml --vault-password-file ansible-vault-password --extra-vars '@vault.yaml'
```

## Reset all Nodes in the Cluster

```
ansible-playbook -i all-hosts reset.yaml --vault-password-file ansible-vault-password --extra-vars '@vault.yaml'
```

## Add SSH Key Certs to known_hosts

```
ansible-playbook -i all-hosts ssh_cert.yaml --vault-password-file ansible-vault-password --extra-vars '@vault.yaml'
```
