install: install-ssh-file setup

install-ssh-file:
	echo "Generating a new ssh key pair pi4.pem"
	ssh-keygen -b 2048 -t rsa -f ./artifacts/pi4.pem -q -N ""
	ansible-playbook install-ssh-key.yaml

setup:
	echo "Waiting to connect to wifi..."
	sleep 60
	ansible-playbook pi.yaml -t all --skip-tags "zulu-umount,stop-syncthing"

mount:
	ansible-playbook -t zulu-mount

unmount:
	ansible-playbook -t zulu-unmount
