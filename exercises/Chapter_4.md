# Chapter 4 Exercise Problems

### 1.

Install a new software package from the m-fadl repository.

---

```shell
root@Fadl:/# apt-get install synaptic
Reading package lists... Done
Building dependency tree
Reading state information... Done
...........
...........
```

---

### 2.

Remove that same software package.

---

```shell
root@Fadl:/# apt-get remove synaptic
Reading package lists... Done
Building dependency tree
Reading state information... Done
..............
..............
```

---

### 3.

Update your repository.

---

```shell
root@Fadl:/# apt-get update

Get:1 http://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]
Get:3 http://dl.google.com/linux/chrome/deb stable/main amd64 Packages [1,095 B]
Get:2 http://kali.download/kali kali-rolling InRelease [30.5 kB]
Get:4 http://kali.download/kali kali-rolling/main amd64 Packages [17.5 MB]
Get:5 http://kali.download/kali kali-rolling/contrib amd64 Packages [106 kB]
Get:6 http://kali.download/kali kali-rolling/non-free amd64 Packages [202 kB]
Fetched 17.8 MB in 9s (2,077 kB/s)
Reading package lists... Done
```

---

### 4.

Upgrade your software packages.

---

```shell
root@Fadl:/# apt-get update

Reading package lists... Done
Building dependency tree
Reading state information... Done
Calculating upgrade... Done
..............
..............

```

---

### 5.

Select a new piece of software from github and clone it to your system.

---

```shell
m-fadl@Fadl:~$ git clone https://github.com/mohamedfadl285/Cyber-Security-Circle-Linux-Task.git
Cloning into 'Cyber-Security-Circle-Linux-Task'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 12 (delta 2), reused 11 (delta 1), pack-reused 0
Unpacking objects: 100% (12/12), 4.55 KiB | 1.14 MiB/s, done.
```

---
