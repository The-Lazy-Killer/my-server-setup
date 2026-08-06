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
Installation based on: https://help.ui.com/hc/en-us/articles/34210126298775-Self-Hosting-UniFi#h_01K2Q77CWHFK6SRG8RR07SNBKQ

Current specs:
* Disk: 20GB
* RAM: 2GB
* vCPU: 1s 2c

Required packages:
* podman 
* slirp4netns
```bash
sudo apt-get update && sudo apt-get install podman slirp4netns
```
Obtain latest download link from: https://ui.com/download

Download package to whatever folder you want
I download to user homedir.

```bash
curl -O https://fw-download.ubnt.com/data/unifi-os-server/f5e2-linux-x64-5.1.21-a400c9c6-8328-4634-b223-ebfcf742720a.21-x64
```

Make file executable
```bash
chmod +x f5e2-linux-x64-5.1.21-a400c9c6-8328-4634-b223-ebfcf742720a.21-x64
```
Start installation
```bash
sudo ./f5e2-linux-x64-5.1.21-a400c9c6-8328-4634-b223-ebfcf742720a.21-x64
```

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
