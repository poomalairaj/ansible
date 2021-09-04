# Ansible scipt to configure Raspberry pi thinclient

This ansible playbook configures my Raspberry pi 3 which is used as a thinclient. Just basic packages and configurations needed to run as an RDP client.

**Important:** This ansible configures raspberry pi with ultra-wide monitor HDMI with resolution of 2560x1080

## Manual changes
* Write the raspberry pi image to the sd card
* Install ansible and git
```
sudo apt update && sudo apt install ansible git -y
```
* Clone this repository
```
git clone github.com/poomalairaj/ansible
```
* Run the playbook
```
cd ansible/playbook/pi_thinclient
ansible-playbook pi_thinclient.yaml
```
