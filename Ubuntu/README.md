# Documentation

Ubuntu
---
Display version
```sh
cat /etc/issue
lsb_release -a
 ```

Take a screenshot
```sh
import -window root -quality 98 screenshot.png
```

Prevent screen from locking
```sh
gsettings set org.gnome.desktop.session idle-delay 0
```

All processes
```sh
top
```

## User management

List all groups [[*]](http://stackoverflow.com/questions/14059916/is-there-a-command-to-list-all-unix-group-names)
```sh
groups
cut -d: -f1 /etc/group
```

List all users [[*]](http://askubuntu.com/questions/410244/a-command-to-list-all-users-and-how-to-add-delete-modify-users)
```sh
cut -d: -f1 /etc/passwd
```

Add a new user
```sh
sudo adduser new_username
```


See which groups your linux user belongs to[[*]](http://www.howtogeek.com/howto/ubuntu/see-which-groups-your-linux-user-belongs-to/)
```sh
groups username
```

Change password [[*]](http://www.cyberciti.biz/faq/linux-set-change-password-how-to/)
```sh
passwd new_username
```

Remove a user, option r removes the user's home directory [[*]](http://www.cyberciti.biz/faq/linux-remove-user-command/)
```sh
userdel -r username
```


Centos
---
## OpenSSH
Restart ssh service [[*]](http://wiki.centos.org/HowTos/Network/SecuringSSH)
```sh
service sshd restart
```

In sshd_config
```sh
AuthorizedKeysFile      .ssh/authorized_keys
```

Ssh mode verbose
```sh
ssh -vvv root@address.com
```
