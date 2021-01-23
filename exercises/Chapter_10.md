# Chapter 10 Exercise Problems

### 1.

Use the `mount` and `umount` commands to mount and unmount your flash drive.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  mount /dev/sdb1 /media

┌──(m-fadl㉿Fadl)-[~]
└─$  umount /dev/sdb1
```

---

### 2.

Check the amount of disk space free on your primary hard drive.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  df

Filesystem     1K-blocks    Used Available Use% Mounted on
udev              328680       0    328680   0% /dev
tmpfs              72184    1172     71012   2% /run
/dev/sda1       11544760 9677432   1261172  89% /
tmpfs             360904       0    360904   0% /dev/shm
tmpfs               5120       0      5120   0% /run/lock
tmpfs               4096       0      4096   0% /sys/fs/cgroup
tmpfs              72180      52     72128   1% /run/user/1000
```

---

### 3.

Check for errors on your flash drive with `fsck`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  fsck -p /dev/sdb1
--snip--
```

---

### 4.

Use the `dd` command to copy the entire contents of one flash drive to another, including deleted files.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  dd if=/dev/sdb1 of=/dev/sdc1
--snip--
```

---

### 5.

Use the `lsblk` command to determine basic characteristics of your block devices.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  lsblk

NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   12G  0 disk
├─sda1   8:1    0 11.2G  0 part /
├─sda2   8:2    0    1K  0 part
└─sda5   8:5    0  766M  0 part [SWAP]
sr0     11:0    1 1024M  0 rom
```

---
