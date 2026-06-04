# Bandit Level 10

> The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit10@bandit.labs.overthewire.org -p 2220
```

```shell
base64 -d data.txt 
```

```text
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

