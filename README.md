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
"chris@ubuntu:~$ groups chris
chris : chris sudo docker
chris@ubuntu:~$ sudo !!
sudo groups chris
chris : chris sudo docker
chris@ubuntu:~$ "
```

To cat out all the groups:  ```cat /etc/group```

To get name of the machine ```hostname``` 
Output : 
```
chris@ubuntu:~$ hostname
ubuntu
```

To change the prompt from ```chris@ubuntu:~$``` to ```MyNewPrompt $``` :
```
echo $PS1
PS1="MyNewPrompt $ "
```
Now echoing $PS1 again will give output as static value as ```MyNewPrompt $```
like :
```
MyNewPrompt $ echo $PS1
MyNewPrompt $
```
