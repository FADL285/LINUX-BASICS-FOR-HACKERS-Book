# Chapter 11 Exercise Problems

### 1.

Use the `locate` command to find all the `rsyslog` files.

---

```shell
m-fadl@Fadl:~$ locate rsyslog
/etc/rsyslog.conf
/etc/rsyslog.d
/etc/init.d/rsyslog
/etc/logcheck/ignore.d.server/rsyslog
/etc/logrotate.d/rsyslog
/etc/rc0.d/K01rsyslog
/etc/rc1.d/K01rsyslog
/etc/rc2.d/S01rsyslog
/etc/rc3.d/S01rsyslog
/etc/rc4.d/S01rsyslog
/etc/rc5.d/S01rsyslog
/etc/rc6.d/K01rsyslog
/etc/systemd/system/multi-user.target.wants/rsyslog.service
/usr/lib/rsyslog
...............
...............
```

---

### 2.

Open the `rsyslog.conf` file and change your log rotation to one week.

---

```shell
m-fadl@Fadl:~$ vi /etc/rsyslog.conf

--snip--
```

```shell
m-fadl@Fadl:~$ vi /etc/logrotate.conf

--snip--
```

---

### 3.

Disable logging on your system. Investigate what is logged in the file `/var/log/syslog` when you disable logging.

---

```shell
root@Fadl:/# service rsyslog stop

Warning: Stopping rsyslog.service, but it can still be 
..........
..........
```

---

### 4.

Use the `shred` command to shred and delete all your `kern` log files.

---

```shell
root@Fadl:/# cat /etc/rsyslog.conf | grep kern

module(load="imklog")   # provides kernel logging support
kern.*                          -/var/log/kern.log

root@Fadl:/# shred -f -n 10 /var/log/kern.log
```

---
