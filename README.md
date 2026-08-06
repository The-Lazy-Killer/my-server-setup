# my-server-setup
Just another server setup stored in Github


## Proxmox VE
### Setup and configuration


## VMs
Usually Ubuntu Server LTS

### Docker Hosts

#### Portainer

### Unifi OS Server

Unifi OS server

Current specs:
* Disk: 20GB
* RAM: 2GB
* vCPU: 1s 2c




## Default VM Configurations

Update repos, upgrade packages and reboot server.
```bash
sudo apt update -y && sudo apt upgrade -y && sudo reboot -y
```

Install packages I use
```bash
sudo apt install -y qemu-guest-agent \
                 ufw  
```

Enable and start qemu-agent
```bash
sudo systemctl enable qemu-guest-agent && sudo systemctl start qemu-guest-agent
```
