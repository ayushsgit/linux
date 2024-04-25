# linux
commands

To Add user: man useradd //opens the manual of useradd command
```
useradd -D -s /bin/bash
useradd -m chris
passwd chris
usermod -aG sudo chris
su - chris
```

To add group:
```
groupadd docker
sudo usermod -aG docker $USER
echo $USER //echoes the current user
groups chris //to see what groups chris is associated with like
"luff@ubuntu:~$ groups luff
luff : luff sudo docker
luff@ubuntu:~$ sudo !!
sudo groups luff
luff : luff sudo docker
luff@ubuntu:~$ "
```

To cat out all the groups:  ```cat /etc/group```
