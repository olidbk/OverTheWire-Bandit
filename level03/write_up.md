# Bandit Level 3

> The password for the next level is stored in a hidden file in the **inhere** directory.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit3@bandit.labs.overthewire.org -p 2220
```

```shell
cd inhere
ls -a
```

```shell
cat ./...Hiding-From-You
```

```text
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

