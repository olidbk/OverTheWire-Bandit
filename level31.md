# Bandit Level 31

> There is a git repository at `ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

## Login

```shell
ssh bandit31@bandit.labs.overthewire.org -p 2220

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
```

## Solution

**in your machine you have to clone the repo on port 2220 and the password is same**

```shell
cd repo
cat README.md
```

```text
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master
```

**so we have to push a file to the remote repository**

```shell
echo "May I come in?" > key.txt
```

```shell
git add key.txt
```

```text
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Disable this message with "git config set advice.addIgnoredFile false"
```

**so the gitignore stop us from add the file**

```shell
cat .gitignore
```

```text
*.txt
```

**we have to add '-f' parameter to force it**

```shell
git add key.txt -f
```

**then commit it**

```shell
git commit -a
```

**then push it**

```shell
git push -u origin master
```

```text
3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
```

