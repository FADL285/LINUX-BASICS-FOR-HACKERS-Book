# Chapter 14 Exercise Problems

### 1.

Check your network devices with `ifconfig`. Note any wireless extensions.

---

```shell
root@Fadl:/home/m-fadl# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.16.194.131  netmask 255.255.255.0  broadcast 172.16.194.255
        inet6 fe80::20c:29ff:fef6:8ef2  prefixlen 64  scopeid 0x20<link>
        ether 00:0c:29:f6:8e:f2  txqueuelen 1000  (Ethernet)
        RX packets 19985  bytes 22772474 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9721  bytes 759307 (741.5 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 140879  bytes 16626410 (15.8 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 140879  bytes 16626410 (15.8 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

---

### 2.

Run `iwconfig` and note any wireless network adapters.

---

```shell
root@Fadl:/home/m-fadl# iwconfig
lo        no wireless extensions.

eth0      no wireless extensions.
```

---

### 3.

Check to see what Wi-Fi AP's are in range with `iwlist`.

---

```shell
root@Fadl:/home/m-fadl# iwlist wlan0 scan
--snip--
```

---

### 4.

Check to see what Wi-Fi AP's are in range with `nmcli`. Which do you find more useful and intuitive, `nmcli` or `iwlist`?

---

```shell
root@Fadl:/home/m-fadl# nmcli dev wifi
--snip--
```

---

### 5.

Connect to your Wi-Fi AP using `nmcli`.

---

```shell
root@Fadl:/home/m-fadl# nmcli dev wifi connect FADL password @m3n@z@F!
--snip--
```

---

### 6.

Bring up your Bluetooth adapter with `hciconfig` and scan for nearby discoverable Bluetooth devices with `hcitool`.

---

```shell
root@Fadl:/home/m-fadl# hciconfig hci0 up
root@Fadl:/home/m-fadl# hcitool scan
--snip--
```

---

### 7.

Test whether those Bluetooth devices are within reachable distance with `l2ping`.

---

```shell
root@Fadl:/home/m-fadl# l2ping 76:6E:46:63:72:66 -c 3
--snip--
```

---
