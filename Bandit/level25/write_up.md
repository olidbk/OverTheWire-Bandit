# Bandit Level 25

> Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit25@bandit.labs.overthewire.org -p 2220
```

**first, we need to check what shell the user bandit26 used**

```shell
cat /etc/passwd | grep bandit26
```

```text
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
```

```shell
cat /usr/bin/showtext
```

```shell
#!/bin/sh

export TERM=linux

more ~/text.txt
exit 0
```

**we can see that it refers to a script called 'showtext' that opens a file called 'text.txt' with the 'more' program**

**next, when we look in the home directory of the current user, we find a private ssh key**

```shell
ls
bandit26.sshkey
```

so we have to copy the file in a new terminal and change his permissions with `chmod 600 bandit26.sshkey`, then try  to connect

```shell
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
```

**when trying to log in, we see that the connection is closed because '/usr/bin/showtext' is executed**

**what exactly has happened? The text in ’text.txt’ is very short, meaning the whole text can immediately be displayed. `more` does not need to go into command/interactive mode. if we make the terminal window smaller, `more` will go into command mode. we can then use `v` to go into vim. now we can rescale the terminal**

**Vim is now opened as 'bandit26'. so to find the password we need first to set the default shell of the user in vim to a useful shell, like `\bin\bash`. the commands look like the following: `:set shell=/bin/bash` and then use `:shell`. finally, we have a shell of `bandit26@bandit:~$` and can get the password for the user**

```shell
cat /etc/bandit\_pass/bandit26
```

```text
s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
```

