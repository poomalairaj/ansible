# Ansible scipt to configure mint VM

* Install mint in vm
* Install ssh

```
sudo apt update && sudo apt install ssh python -y
```

Create ssh key pair from the pi-thinclient

```
ssh-keygen -t ecdsa -f ~/.ssh/mint
ssh-copy-id -i ~/.ssh/mint.pub mint@192.168.1.100
copy ~/.ssh/mint ~/projects/ansible/playbook/vm/artifacts
```
* Before running the play book make sure that sudo doesn't ask password.
Put the following line in visudo

```
mint ALL=(ALL) NOPASSWD: ALL
```

* Run the playbook

```
cd ansible/playbook/vm
ansible-playbook vm.yaml
```
