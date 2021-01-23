# Chapter 15 Exercise Problems

### 1.

Check the version of your kernel.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  uname -a

Linux Fadl 5.9.0-kali4-amd64 #1 SMP Debian 5.9.11-1kali1 (2020-12-01) x86_64 GNU/Linux
```

---

### 2.

List the modules in your kernel.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  lsmod

Module                  Size  Used by
vsock_loopback         16384  0
vmw_vsock_virtio_transport_common    40960  1 vsock_loopback
vmw_vsock_vmci_transport    32768  2
vsock                  49152  7
................
................
```

---

### 3.

Enable IP forwarding with a `sysctl` command.

---

```shell
┌──(root💀Fadl)-[~]
└─# sysctl -w net.ipv4.ip_forward=1

net.ipv4.ip_forward = 1
```

---

### 4.

Edit your `/etc/sysctl.conf` file to enable IP forwarding. Now, disable IP forwarding.

---

```shell
┌──(root💀Fadl)-[~]
└─# vi /etc/sysctl.conf

--snip--
sysctl -w net.ipv4.ip_forward=0
net.ipv4.ip_forward = 0
```

---

### 5.

Select one kernel module and learn more about it using `modinfo`.

---

```shell
┌──(root💀Fadl)-[~]
└─# modinfo bluetooth

filename:       /lib/modules/5.7.0-m-fadl1-amd64/kernel/net/bluetooth/bluetooth.ko
alias:          net-pf-31
license:        GPL
version:        2.22
description:    Bluetooth Core ver 2.22
............
............
```

---
