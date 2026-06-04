# Bandit Level 32

> After all this `git` stuff, it’s time for another escape. Good luck!

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit32@bandit.labs.overthewire.org -p 2220
```

```shell
WELCOME TO THE UPPERCASE SHELL
>> whoami
sh: 1: WHOAMI: Permission denied
```

**here we see that we are in a shell that change all our commands to uppercase**

**the one thing in Linux that is uppercase is variables. specifically, the variable `$0` has a reference to a shell. you can see this with `echo $0` on your machine**
**this lets us break out of the uppercase shell and we can use commands again**

```shell
cat /etc/bandit\_pass/bandit33
```

```text
tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0
```

