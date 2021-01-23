# Chapter 3 Exercise Problems

### 1.

Find information on your active network interfaces.

---

```shell
root@Fadl:/# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.16.194.131  netmask 255.255.255.0  broadcast 172.16.194.255
        inet6 fe80::20c:29ff:fef6:8ef2  prefixlen 64  scopeid 0x20<link>
        ether 00:0c:29:f6:8e:f2  txqueuelen 1000  (Ethernet)
        RX packets 20030  bytes 22782431 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9752  bytes 762993 (745.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141024  bytes 16678770 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141024  bytes 16678770 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

---

### 2.

Change the IP address on `eth0` to `192.168.1.1`.

---

```shell
root@Fadl:/# ifconfig eth0 194.168.1.1/24
root@Fadl:/# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 194.168.1.1  netmask 255.255.255.0  broadcast 194.168.1.255
        inet6 fe80::20c:29ff:fef6:8ef2  prefixlen 64  scopeid 0x20<link>
        ether 00:0c:29:f6:8e:f2  txqueuelen 1000  (Ethernet)
        RX packets 20032  bytes 22782821 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9752  bytes 762993 (745.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141036  bytes 16683122 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141036  bytes 16683122 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

---

### 3.

Change your hardware address on `eth0`.

---

```shell
root@Fadl:/# ifconfig eth0 down
root@Fadl:/# ifconfig eth0 hw ether 00:11:22:33:44:55
root@Fadl:/# ifconfig eth0 up
root@Fadl:/# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 194.168.1.1  netmask 255.255.255.0  broadcast 194.168.1.255
        inet6 fe80::211:22ff:fe33:4455  prefixlen 64  scopeid 0x20<link>
        ether 00:11:22:33:44:55  txqueuelen 1000  (Ethernet)
        RX packets 20033  bytes 22783016 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9756  bytes 763389 (745.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141073  bytes 16696314 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141073  bytes 16696314 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

---

### 4.

Check whether you have any available wireless interfaces active.

---

```shell
root@Fadl:/# iwconfig
lo        no wireless extensions.

eth0      no wireless extensions.
```

---

### 5.

Reset your IP address to a DHCP-assigned address.

---

```shell
root@Fadl:/# dhclient eth0
root@Fadl:/# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.16.194.132  netmask 255.255.255.0  broadcast 172.16.194.255
        inet6 fe80::211:22ff:fe33:4455  prefixlen 64  scopeid 0x20<link>
        ether 00:11:22:33:44:55  txqueuelen 1000  (Ethernet)
        RX packets 20045  bytes 22784936 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9764  bytes 764752 (746.8 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141093  bytes 16702920 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141093  bytes 16702920 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

---

### 6.

Find the nameserver and email server of your favorite website.

---

```shell
m-fadl@Fadl:~$ dig github.com ns
--snip--
;; QUESTION SECTION:
;github.com.                    IN      NS

;; ANSWER SECTION:
github.com.             5       IN      NS      ns-1707.awsdns-21.co.uk.
github.com.             5       IN      NS      ns-421.awsdns-52.com.
github.com.             5       IN      NS      ns-520.awsdns-01.net.
github.com.             5       IN      NS      dns1.p08.nsone.net.
github.com.             5       IN      NS      dns2.p08.nsone.net.
github.com.             5       IN      NS      dns3.p08.nsone.net.
github.com.             5       IN      NS      dns4.p08.nsone.net.
github.com.             5       IN      NS      ns-1283.awsdns-32.org.

;; ADDITIONAL SECTION:
dns1.p08.nsone.net.     5       IN      A       198.51.44.8
dns2.p08.nsone.net.     5       IN      A       198.51.45.8
dns3.p08.nsone.net.     5       IN      A       198.51.44.72
dns4.p08.nsone.net.     5       IN      A       198.51.45.72
ns-1283.awsdns-32.org.  5       IN      A       205.251.197.3
ns-1283.awsdns-32.org.  5       IN      AAAA    2600:9000:5305:300::1
ns-1707.awsdns-21.co.uk. 5      IN      A       205.251.198.171
ns-1707.awsdns-21.co.uk. 5      IN      AAAA    2600:9000:5306:ab00::1
ns-421.awsdns-52.com.   5       IN      A       205.251.193.165
ns-421.awsdns-52.com.   5       IN      AAAA    2600:9000:5301:a500::1
ns-520.awsdns-01.net.   5       IN      A       205.251.194.8
ns-520.awsdns-01.net.   5       IN      AAAA    2600:9000:5302:800::1
--snip--
```

---

### 7.

Add Google's DNS server to your `/etc/resolv.conf` file so your system refers to that server when it can't resolve a domain name query with your local DNS server.

---

```shell
root@Fadl:/# echo "nameserver 8.8.8.8" >> /etc/resolv.conf
```

---
