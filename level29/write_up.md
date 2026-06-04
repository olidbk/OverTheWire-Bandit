# Bandit Level 29

> There is a git repository at `ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

## Solution

**in your machine you have to clone the repo on port 2220 and the password is same**

```shell
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
```

```shell
cd repo
cat README.md
```

```text
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>
```

**after checking a wile we will notice that we have to check the branches and deleted branches**

```shell
git branch -a
```

```shell
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
```

```shell
git checkout dev
```

```shell
ls
cat README.md
```

```text
cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
```

```text
qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
```

