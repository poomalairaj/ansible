# Ansible scipt to configure mint VM

* Install mint in vm
* Install ssh

```
sudo apt update && sudo apt install ssh -y
```

Create ssh key pair from the pi-thinclient

```
ssh-keygen -t ecdsa -f ~/.ssh/mint
ssh-copy-id -i ~/.ssh/mint.pub mint@192.168.1.100
copy ~/.ssh/mint ~/projects/ansible/playbook/vm/artifacts
```


```
* Run the playbook
```
cd ansible/playbook/pi_thinclient
ansible-playbook pi_thinclient.yaml
```
