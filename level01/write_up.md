# Bandit Level 1

> The password for the next level is stored in a file called **-** located in the home directory

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit1@bandit.labs.overthewire.org -p 2220
```

**the terminal think the '-' as a switche, so you need to specify it**

```sehll
cat ./-
```

```text
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

