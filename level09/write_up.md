# Bandit Level 9

> The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit9@bandit.labs.overthewire.org -p 2220
```

```shell
strings data.txt | grep "==="
```

```text
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

