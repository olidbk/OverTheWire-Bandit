# Bandit Level 13

> The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.  
   If you need help with this level: a hint file can be found in the home directory.  
   Make sure to read the error messages as they are informative.

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit13@bandit.labs.overthewire.org -p 2220
```

**first copy the sshkey_privet file from bandit13 to your local machine using 'scp' (secure copy). you need to use the 'scp' command in your local machin**

```shell
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
```

**then you have to enter the password for bandit13**

```text
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

**change the permissions to 600 so you can use ssh with the privet key file**

```shell
chmod 600 sshkey.private
```

**and now you can connect to the next level**

```shell
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

