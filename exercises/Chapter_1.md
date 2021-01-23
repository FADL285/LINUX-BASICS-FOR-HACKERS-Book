# Chapter 1 Exercise Problems

### 1.

Use the `ls` command from the root (`/`) directory to explore the directory structure of Linux. Move to each of the directories with the `cd` command and run `pwd` to verify where you are in the directory structure.

---

```shell
root@Fadl:/# ls -l

root@Fadl:/# cd boot/
root@Fadl:/boot# pwd
/boot

root@Fadl:/boot# cd /dev/
root@Fadl:/dev# pwd
/dev

root@Fadl:/dev# cd /etc/
root@Fadl:/etc# pwd
/etc

etc .........
```

---

### 2.

Use the `whoami` command to verify which user you are logged in as.

---

```shell
m-fadl@Fadl:~$ whoami
m-fadl
```

---

### 3.

Use the `locate` command to find wordlists that can be used for password cracking.

---

```shell
m-fadl@Fadl:~$ locate wordlists
/usr/bin/wordlists
/usr/lib/python3/dist-packages/theHarvester/wordlists
/usr/share/wordlists
/usr/share/amass/wordlists
/usr/share/amass/wordlists/all.txt
/usr/share/amass/wordlists/bitquark_subdomains_top100K.txt
/usr/share/amass/wordlists/deepmagic.com_top500prefixes.txt
--snip--
/var/lib/dpkg/info/wordlists.prerm
```

---

### 4.

Use the `cat` command to create a new file and then append to that file. Keep in mind that `>` redirects input to a file and `>>` appends to a file.

---

```shell
m-fadl@Fadl:~$ cat > newfile
This is my new file.
m-fadl@Fadl:~$ cat >> newfile
This is my appendage.
m-fadl@Fadl:~$ cat newfile
This is my new file.
This is my appendage.
```

---

### 5.

Create a new directory called `hackerdirectory` and create a new file that directory named `hackedfile`. Now copy that file to your `/root` directory and rename it `secretfile`.

---

```shell
root@Fadl:/home/m-fadl# mkdir hackerdirectory
root@Fadl:/home/m-fadl# touch hackerdirectory/hackedfile
root@Fadl:/home/m-fadl# cp hackerdirectory/hackedfile /root/secretfile
```

---
