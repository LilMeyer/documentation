# Documentation

Ubuntu
---
Display version
```sh
cat /etc/issue
lsb_release -a
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


Show all services
```sh
service --status-all
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


References
---
- [Centos OpenSSH](http://wiki.centos.org/HowTos/Network/SecuringSSH)
