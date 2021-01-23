# Chapter 2 Exercise Problems

### 1.

Navigate to `/usr/share/metasploit-framework/data/wordlists`. This is a directory of multiple wordlists that can be used to brute force passwords in various password-protected devices using Metasploit, the most popular pentesting and hacking framework.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  cd /usr/share/metasploit-framework/data/wordlists/
```

---

### 2.

Use the `cat` command to view the contents of the file `password.lst`.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ cat password.lst

!@#$%
!@#$%^
!@#$%^&
!@#$%^&*
!boerbul
--snip--
vagrant
```

---

### 3.

Use the `more` command to display the file `password.lst`.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ more password.lst

--snip--
```

---

### 4.

Use the `less` command to view the file `password.lst`.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ less password.lst

--snip--
```

---

### 5.

Now use the `nl` command to place line numbers on the passwords in `password.lst`. There should be around `88,396` passwords.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ nl password.lst

 00001 !@#$%
 00002 !@#$%^
 00003 !@#$%^&
 00004 !@#$%^&*
 00005 !boerbul
--snip--
 88397 vagrant
```

---

### 6.

Use the `tail` command to see the last `20` passwords in `password.lst`.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ tail -20 password.lst

zxcvbnm
zydeco
zygote
zygotic
zymurgy
zyrtec
zyuganov
zzz
z�rich
�gar
�ngstr�m
�clair
�clairs
�clat
�lan
�migr�
�migr�s
�p�e
�tude
vagrant
```

---

### 7.

Use the `cat` command to display `password.lst` and pipe it to find all the passwords that contain `123`.

---

```shell
┌──(m-fadl㉿Fadl)-[/usr/share/metasploit-framework/data/wordlists]
└─$ cat password.lst | grep 123

123
123123
123321
1234
12345
123456
1234567
12345678
123456789
1234567890
1234qwer
123abc
123go
123qwe
a12345
abc123
abcd123
abcd1234
aki123
asdf1234
chris123
happy123
hello123
help123
jkl123
red123
test123
xxx123
xyz123
zxc123
```

---
