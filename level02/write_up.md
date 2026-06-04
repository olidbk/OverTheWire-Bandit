# Bandit Level 2

> The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit2@bandit.labs.overthewire.org -p 2220
```

```shell
cat ./--spaces\ in\ this\ filename--
```

```text
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

