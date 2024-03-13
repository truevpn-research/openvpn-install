# Install OpenVPN

## 1. Update your system
First, run the apt command to apply security updates:
```sh
sudo apt update
sudo apt upgrade
```


## 1. Get the Script
First, run the apt command to apply security updates:
```sh
wget https://raw.githubusercontent.com/truevpn-research/openvpn-install/master/openvpn-install.sh -O openvpn-ubuntu-install.sh

```

Required permissions

```sh
chmod -v +x openvpn-ubuntu-install.sh
```

Run openvpn-ubuntu-install.sh script to install OpenVPN server
Now all you have to do is:

```sh
sudo ./openvpn-ubuntu-install.sh
```



We need to use the systemctl command as follows:

Stop the OpenVPN server
```
sudo systemctl stop openvpn-server@server.service
```
## OR when using password to protect vpn ##
```
sudo systemctl stop openvpn@server.service
```

Start the OpenVPN server
```
sudo systemctl start openvpn-server@server.service
```
## OR when using password to protect vpn ##
```
sudo systemctl start openvpn@server.service
```

Restart the OpenVPN server after changing configuration options
```
sudo systemctl restart openvpn-server@server.service
```
## OR when using password to protect vpn ##
```
sudo systemctl restart openvpn@server.service
```

Show status of the OpenVPN server
```
sudo systemctl status openvpn-server@server.service
```
## OR when using password to protect vpn ##
```
sudo systemctl status openvpn@server.service
```

