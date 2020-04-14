## static IP address
add the following lines to `/etc/netplan/50-cloud-init.yaml`

```
network:
    ethernets:
        enp0s25:
            dhcp4: no
            addresses: [192.168.1.110/24]
            gateway4: 192.168.1.1
            nameservers:
              addresses: [192.168.1.1]
              search: []
    version: 2
```
```shell
sudo netplan apply
```

## user directories name
```shell
LANG=C xdg-user-dirs-update
```

## Regolith Linux
[Regolith Linux](https://regolith-linux.org/)


add the Regolith PPA to your existing Ubuntu system and install the regolith-desktop package with the following terminal commands
```shell
sudo add-apt-repository ppa:regolith-linux/release
sudo apt install regolith-desktop
```
