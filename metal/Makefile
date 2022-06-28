.POSIX:

default: boot proxmox

boot:
	@ansible-playbook \
		--inventory hosts.yml \
		boot.yml

requirements:
	@ansible-galaxy install -r requirements.yml

proxmox: requirements
	@ansible-playbook \
		--inventory hosts.yml \
		proxmox.yml
