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

To see hidden file that start with a dot(.) : ```ls -al```

To make this ```MyNewPrompt $``` permanent even after logging out like :
```
MyNewPrompt $ exit
logout
ubuntu $ su - chris
chris@ubuntu:~$
```
We do :
```
echo PS1="MyNewPrompt $ " >> .bashrc
```
To save this we do : ```vim .bashrc``` then type ```i``` to enter insert mode then head down till we find ```PS1=MyNewPrompt $``` and edit it to ```PS1="MyNewPrompt $"``` then hit ```Esc``` key then type ```:wq``` to save and quit vim
Then type ```source .bashrc``` to implement the changes
