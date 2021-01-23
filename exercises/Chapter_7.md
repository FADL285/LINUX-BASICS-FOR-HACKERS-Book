# Chapter 7 Exercise Problems

### 1.

View all of your environment variables with the `more` command.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  set | more

BASH=/bin/bash
BASHOPTS=checkwinsize:cmdhist:complete_fullquote:expand_aliases:extglob:ext
quote:force_fignore:globasciiranges:histappend:interactive_comments:progcom
p:promptvars:sourcepath
BASH_ALIASES=()
BASH_ARGC=([0]="0")
BASH_ARGV=()
--snip--
}
```

---

### 2.

Use the `echo` command to view the `HOSTNAME` variable.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  echo $HOSTNAME

Fadl
```

---

### 3.

Find a method to change the slash (`/`) to a backslash ('\') in the faux Microsoft `cmd PS1` example (see Listing 7.2).

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  PS1='C:\\\W> '

C:\~> cd /home
C:\home>
```

---

### 4.

Create a variable names `MYNEWVARIABLE` and put your name in it.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  MYNEWVARIABLE=mohamedfadl
```

---

### 5.

Use `echo` to view the contents of `MYNEWVARIABLE`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  echo $MYNEWVARIABLE

mohamedfadl
```

---

### 6.

Export `MYNEWVARIABLE` so that it's available in all environments.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  export MYNEWVARIABLE
```

---

### 7.

Use the echo command to view the contents of the `PATH` variable.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  echo $PATH

/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games
```

---

### 8.

Add your home directory to the `PATH` variable so that any binaries in your home directory can be used in any directory.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  PATH=$PATH:/home/m-fadl
```

---

### 9.

Change your `PS1` variable to "World's Greatest Hacker:".

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  PS1="World's Greatest Hacker: "

World's Greatest Hacker:
```

---
