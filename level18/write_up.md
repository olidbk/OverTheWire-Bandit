# Bandit Level 18

> The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit18@bandit.labs.overthewire.org -p 2220
```

**the script will log you out so you need to add your commande with the connection**

```shell
sshpass -f "sshpass" ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

```text
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```
