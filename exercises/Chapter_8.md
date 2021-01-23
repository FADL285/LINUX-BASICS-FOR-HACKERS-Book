# Chapter 8 Exercise Problems

### 1.

Create your own greeting script similar to our `HelloHackersArise` script.

---

```shell
#! /bin/bash

echo "Hello, world!"
```

---

### 2.

Create a script similar to `MySQLscanner.sh` but design it to find systems with Microsoft's SQL server database at port 1433. Call it `MSSQLscanner`.

---

```shell
#! /bin/bash

nmap -sT 192.168.181.0/24 -p 1433 >/dev/null -oG MSSQLscan

cat MSSQLscan | grep open > MSSQLscan2

cat MSSQLscan2
```

---

### 3.

Alter that `MSSQLscanner` script to prompt the user for a starting and ending IP address and the port to search for. Then filter out all the IP addresses where those ports are closed and display only those that are open.

---

```shell
#! /bin/bash

echo "Enter the starting IP address : "
read FirstIP

echo "Enter the last octet of the last IP address : "
read LastOctetIP

echo "Enter the port number you want to scan for : "
read port

nmap -sT $FirstIP-$LastOctetIP -p $port >/dev/null -oG MSSQLscan

cat MSSQLscan | grep open > MSSQLscan2

cat MSSQLscan2
```

---
