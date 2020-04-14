## static IP address
add the following lines to /etc/netplan/50-cloud-init.yaml

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
```
$ sudo netplan apply
```

## user directories name
```shell
LANG=C xdg-user-dirs-update
```
