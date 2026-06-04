# Bandit Level 8

> The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit8@bandit.labs.overthewire.org -p 2220
```

```shell
sort data.txt | uniq -u
```

```text
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

