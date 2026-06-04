# Bandit Level 7

> The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit7@bandit.labs.overthewire.org -p 2220
```

```shell
cat data.txt | grep "millionth"
```

```text
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

