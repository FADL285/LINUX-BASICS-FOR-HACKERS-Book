# Chapter 9 Exercise Problems

### 1.

Create three scripts to combine, similar to what we did in Chapter 8. Name them `Linux4Hackers1`, `Linux4Hackers2`, and `Linux4Hackers3`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  echo $'#! /bin/bash\n\n echo "This is 1"' > Linux4Hackers1

┌──(m-fadl㉿Fadl)-[~]
└─$  echo $'#! /bin/bash\n\n echo "This is 22"' > Linux4Hackers2

┌──(m-fadl㉿Fadl)-[~]
└─$  echo $'#! /bin/bash\n\n echo "This is 333"' > Linux4Hackers3
```

---

### 2.

Create a tarball from these three files. Name the tarball `L4H`. Note how the size of the sum of the three files changes when they are tarred together.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  tar -cf L4H Linux4Hackers1 Linux4Hackers2 Linux4Hackers3

┌──(m-fadl㉿Fadl)-[~]
└─$  ls -l Linux4Hackers? L4H

-rw-r--r-- 1 m-fadl m-fadl 10240 Sep  7 23:19 L4H
-rw-r--r-- 1 m-fadl m-fadl    32 Sep  7 23:16 Linux4Hackers1
-rw-r--r-- 1 m-fadl m-fadl    33 Sep  7 23:16 Linux4Hackers2
-rw-r--r-- 1 m-fadl m-fadl    34 Sep  7 23:16 Linux4Hackers3
```

---

### 3.

Compress the `L4H` tarball with `gzip`. Note how the size of the file changes. Investigate how you can control overwriting existing files. Now uncompress the `L4H` file.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  gzip L4H

┌──(m-fadl㉿Fadl)-[~]
└─$  ls -l L4H.gz
-rw-r--r-- 1 m-fadl m-fadl 212 Sep  7 23:19 L4H.gz

┌──(m-fadl㉿Fadl)-[~]
└─$  gunzip L4H.gz
```

---

### 4.

Repeat Exercise `3` with both `bzip2` and `compress`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  bzip2 L4H

┌──(m-fadl㉿Fadl)-[~]
└─$  ls -l L4H.bz2
-rw-r--r-- 1 m-fadl m-fadl 224 Sep  7 23:19 L4H.bz2

┌──(m-fadl㉿Fadl)-[~]
└─$  bunzip2 L4H.bz2
```

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  compress L4H

┌──(m-fadl㉿Fadl)-[~]
└─$  ls -l L4H.Z
-rw-r--r-- 1 m-fadl m-fadl 416 Sep  7 23:19 L4H.Z

┌──(m-fadl㉿Fadl)-[~]
└─$  uncompress L4H.Z
```

---

### 5.

Make a physical, bit-by-bit copy of one of your flash drives using the `dd` command.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  dd if=/dev/sdb of=/home/m-fadl/flashcopy
--snip--
```

---
