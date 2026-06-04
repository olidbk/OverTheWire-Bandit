# Bandit Level 4

> The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit4@bandit.labs.overthewire.org -p 2220
```

```shell
cd inhere
```

**the 'file' command help you see the data type of the file**

```shell
file ./*
cat ./-file07
```

```text
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

