# Documentation

Ubuntu
---
Display version
```sh
cat /etc/issue
lsb_release -a
 ```

Check the current kernel version
```sh
uname -r
```

Install a package .deb [[*]](http://askubuntu.com/questions/40779/how-do-i-install-a-deb-file-via-the-command-line)
```sh
sudo dpkg -i <deb_package.deb>
```

Uninstall a package
```sh
sudo dpkg -r <deb_package.deb>
```

Take a screenshot
```sh
import -window root -quality 98 screenshot.png
```

Show/hide hidden files in nautilus
```sh
Ctrl + H
```

Prevent screen from locking
```sh
gsettings set org.gnome.desktop.session idle-delay 0
```

All processes
```sh
top
```


## Shells
Fish [[*]](http://hackercodex.com/guide/install-fish-shell-mac-ubuntu/)
Installation
```sh
sudo add-apt-repository ppa:fish-shell/nightly-master
sudo apt-get update
sudo apt-get install fish
```

Change the default shell
```sh
chsh -s /usr/bin/bash
```

## Compression

Extract file
```sh
tar xvzf file.tar.gz
```

Untar cpgz
```sh
gzip -cd <archive_name>.cpgz | cpio -idmv
```


## User management


List all groups [[*]](http://stackoverflow.com/questions/14059916/is-there-a-command-to-list-all-unix-group-names)
```sh
groups                 # OR
cut -d: -f1 /etc/group # OR
getent group
```

List all users [[*]](http://askubuntu.com/questions/410244/a-command-to-list-all-users-and-how-to-add-delete-modify-users)
```sh
cut -d: -f1 /etc/passwd
```

Add a new group

```sh
groupadd group
```

Add a new user
```sh
sudo adduser new_username
```

Add a new user to a group
```sh
useradd -G group username
```

Add a user to a group [[*]](https://wiki.archlinux.org/index.php/users_and_groups)
```sh
gpasswd --add username group
```

Delete password for a user
```sh
passwd --delete username
```

See which groups your linux user belongs to [[*]](http://www.howtogeek.com/howto/ubuntu/see-which-groups-your-linux-user-belongs-to/)
```sh
groups username
```

Change password [[*]](http://www.cyberciti.biz/faq/linux-set-change-password-how-to/)
```sh
passwd new_username
```

Remove a group
```sh
groupdel group
```


Remove a user, option r removes the user's home directory [[*]](http://www.cyberciti.biz/faq/linux-remove-user-command/)
```sh
userdel -r username
```

Get the ip address
```sh
curl -s http://whatismijnip.nl | cut -d " " -f 5
```

Show all services
```sh
service --status-all
```

Stop a service from starting on boot [[*]](http://superuser.com/questions/35151/how-do-i-stop-services-from-starting-on-boot-on-ubuntu)
```sh
sudo update-rc.d -f <service_name> remove
```

Active internet connections
```sh
netstat -tulpn
```

Display all sessions
```sh
w
```

Display all jobs
```sh
initctl list
```

Display opened ports
```sh
lsof -iTCP -sTCP:LISTEN | grep app
```


## OpenSSH

Restart ssh service [[*]](http://wiki.centos.org/HowTos/Network/SecuringSSH)
```sh
service sshd restart # Centos
service ssh restart  # Ubuntu
```

In sshd_config
```sh
AuthorizedKeysFile      .ssh/authorized_keys
```

Ssh mode verbose
```sh
ssh -vvv root@address.com
```
## Space usage
Disk usage
```sh
df -h
```

Memory usage
```sh
free -mh
```

## Wifi networks [[*]](https://help.ubuntu.com/community/WifiDocs/Scan_for_Wireless_Network)
List all interface name of cards
```sh
ls /sys/class/net
```

Scan for open networks
```sh
sudo iwlist <wifi_interface> scan
# example sudo iwlist wlan0 scan
```

List all networks available
```sh
sudo iwlist <wifi_interface> scan | grep ESSID
# example sudo iwlist wlan0 scan | grep ESSID
```
Connect to a specific network
```sh
sudo iwconfig <wifi_interface> essid <essid>
```

### With nmcli [[*]](http://askubuntu.com/questions/461825/connect-to-wifi-from-command-line)
List all saved networks
```sh
nmcli -p con list
```

Connect to a network
```sh
nmcli -p con up id <connection_name> iface <wifi_interface>
# example nmcli -p con up id Transcovo iface wlan0
```


References
---
- [Centos OpenSSH](http://wiki.centos.org/HowTos/Network/SecuringSSH)
