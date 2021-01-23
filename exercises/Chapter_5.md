# Chapter 5 Exercise Problems

### 1.

Select a directory and run a long listing on it. Note the permissions on the files and directory.

---

```shell
m-fadl@Fadl:~$ ls -l

total 40
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Desktop
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Documents
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Downloads
drwxr-xr-x 2 root root 4096 Sep  6 13:53 hackerdirectory
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Music
-rw-r--r-- 1 m-fadl m-fadl   43 Sep  6 13:41 newfile
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Pictures
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Public
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Templates
drwxr-xr-x 2 m-fadl m-fadl 4096 Sep  6 12:48 Videos
```

---

### 2.

Select a file you don't have permission to execute and give yourself execute permissions using the `chmod` command. Try using both the numerical method (`777`) and the UGO method.

---

```shell
m-fadl@Fadl:~$ chmod 777 ~/newfile
m-fadl@Fadl:~$ ls -l ~/newfile

-rwxrwxrwx 1 m-fadl m-fadl 43 Sep  6 13:41 /home/m-fadl/newfile

m-fadl@Fadl:~$ chmod g-w,o-wx ~/newfile
m-fadl@Fadl:~$ ls -l ~/newfile

-rwxr-xr-- 1 m-fadl m-fadl 43 Sep  6 13:41 /home/m-fadl/newfile
```

---

### 3.

Choose another file and change its ownership using `chown`.

---

```shell
root@Fadl:/# chown root ./newfile
root@Fadl:/# ls -l ./newfile

-rwxrwxrwx 1 root m-fadl 43 Sep  6 13:41 ./newfile
```

---

### 4.

Use the `find` command to find all files with the `SGID` bit set.

---

```shell
root@Fadl:/# find / -perm -2000

/etc/ppp/peers
/etc/chatscripts
/var/local
/var/log/mysql
/var/log/journal
/var/log/journal/e9b560b98f414f91aa99c7bb7c6945de
/var/mail
/run/postgresql
/run/log/journal
..............
..............
```

---
