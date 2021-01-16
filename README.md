# CAT CyberSecurity Circle Linux Task

![CAT Logo](img/icon.png)

| 📝Chapter  | 🔎Content |
| --- | --- |
| [What is the task](#what-is-the-task) | What is needed from us in this task |
| [Book Details](#book-details) | Some info about the book |
| [Introduction](#introduction) | An introduction to the  book content |
| [Chapter #1](#chapter-1) | GETTING STARTED WITH THE BASICS |
| [Chapter #2](#chapter-2) | TEXT MANIPULATION |
| [Chapter #3](#chapter-3) | ANALYZING AND MANAGING NETWORKS |

---

# What is the task:

> we are asked to make a summary for [LINUX BASICS FOR HACKERS Book](http://bit.ly/2Kn93MS) 👨🏻‍💻👨🏻‍💻

![Book Cover](img/book-cover.png) <br/>

<p align="center">
  <b><a href="http://bit.ly/2Kn93MS">LINUX BASICS FOR HACKERS Book</a></b>
</p>

---

# Book Details:

**This practical, tutorial-style book uses the Kali Linux distribution to teach Linux basics with a focus on how hackers would use them. Topics include Linux command line basics, filesystems, networking, BASH basics, package management, logging, and the Linux kernel and drivers.**

If you're getting started along the exciting path of hacking, cybersecurity, and pentesting, Linux Basics for Hackers is an excellent first step. Using Kali Linux, an advanced penetration testing distribution of Linux, you'll learn the basics of using the Linux operating system and acquire the tools and techniques you'll need to take control of a Linux environment.

First, you'll learn how to install Kali on a virtual machine and get an introduction to basic Linux concepts. Next, you'll tackle broader Linux topics like manipulating text, controlling file and directory permissions, and managing user environment variables. You'll then focus in on foundational hacking concepts like security and anonymity and learn scripting skills with bash and Python. Practical tutorials and exercises throughout will reinforce and test your skills as you learn how to:

- Cover your tracks by changing your network information and manipulating the rsyslog logging utility
- Write a tool to scan for network connections, and connect and listen to wireless networks
- Keep your internet activity stealthy using Tor, proxy servers, VPNs, and encrypted email
- Write a bash script to scan open ports for potential targets
- Use and abuse services like MySQL, Apache web server, and OpenSSH
- Build your own hacking tools, such as a remote video spy camera and a password cracker

Hacking is complex, and there is no single way in. Why not start at the beginning with Linux Basics for Hackers?

---

# Introduction

Hacking is the most important skill set of the 21st century! Nations are spying on each other to gain secrets, cyber criminals are stealing billions of dollars, digital worms demanding ransoms are being released, adversaries are influencing each other’s elections, and combatants are taking down each other’s utilities. These are all the work of hackers, and their influence over our increasingly digital world is just beginning to be felt.

Any person who wants to become a professional hacker must know Linux and know how to deal with this OS because Almost all the best hacker tools are written for Linux, so some basic Linux skills are a prerequisite to becoming a professional hacker.

---

# Chapter #1

> This chapter will teach you how to use the file system and the terminal, and give you some basic commands.

## GETTING STARTED WITH THE BASICS

## Some Concepts:

- **_Binaries :-_** Binaries This term refers to files that can be executed, similar to executables in Windows. Binaries generally reside in the /usr/bin or usr/sbin directory and include utilities such as ps, cat, ls, and cd as well as applications such as the wireless hacking tool aircrack­ng and the intrusion detection system (IDS) Snort.

- **_Directory :-_** This is the same as a folder in Windows. A directory provides a way of
  organizing files, usually in a hierarchical manner.

- **_Home :-_** Each user has their own /home directory, and this is generally where files you
  create will be saved by default.

- **_root :-_** is the user name or account that by default has access to all commands and files on a Linux or other Unix-like operating system. It is also referred to as the root account, root user and the superuser.

- **_Script :-_** This is a series of commands run in an interpretive environment that converts
  each line to source code.

- **_Shell :-_** is the command interpreter in an operating system such as Unix or GNU/Linux, it is a program that executes other programs. It provides a computer user an interface to the Unix/GNU Linux system so that the user can run different commands or utilities/tools with some input data.

- **_Terminal :-_** is a command line interface (CLI).

## Linux Filesystem:

The Linux filesystem structure is somewhat different from that of Windows. Linux doesn’t have a physical drive (such as the C: drive) at the base of the filesystem but uses
a logical filesystem instead. At the very top of the filesystem structure is / (root)

![CAT Logo](img/file-system.png)

> Linux Filesystem

- **/root** The home directory of the all­powerful root user

- **/etc** Generally contains the Linux configuration files—files that control when and how
  programs start up

- **/home** The user’s home directory

- **/mnt** Where other filesystems are attached or mounted to the filesystem

- **/media** Where CDs and USB devices are usually attached or mounted to the filesystem

- **/bin** Where application binaries (the equivalent of executables in Microsoft Windows)
  reside

- **/lib** Where you’ll find libraries (shared programs that are similar to Windows DLLs)

## BASIC COMMANDS IN LINUX

- Finding Yourself with **pwd**

  `pwd` => return the present working directory

- Checking Your Login with **whoami**

  `whoami` => return the user which logged in

- Changing Directories with **cd**

  `cd dirName` => change the directory to dirName directory

  `cd ..` => move up one level in the file structure

- Listing the Contents of a Directory with **ls**

  `ls` => return the contents of current directory (files and directories)

  we can add **arguments (flags)** to `ls` command to see extra information such as `ls -l` this get more information about the files and directories, such as their permissions, owner, size, and when they were last modified.

  or `-R` flag to list Subdirectories recursively

- Getting Help: Nearly every command, application, or utility has a dedicated help file in Linux that
  provides guidance for its use.

  to get help for specific commands, add `--help` to get the help ex:

  ` ls --help` => return short description of the tool and guidance on how to use it.

- Referencing Manual Pages with **man**

  In addition to the help switch, most commands and applications have a manual (man) page with more information, such as a description and synopsis of the command or application. You can view a man page by simply typing manbefore the command, utility, or application.

  `man nmap` => opens the manual for nmap, providing you with more detailed information than the helpscreen.

- Creating Files

  1. with **touch**

     `touch file.txt` => create a text file

  2. with **cat**

     `cat > file.txt` => create a write on it ( to exit write mode click `ctrl + D` )

- Showing File Content with **cat**

  `cat fileName` => return file content

- Creating a Directory with **mkdir**

  `mkdir newDirectory` => create a new directory

- Copying a File with **cp**

  `cp oldfile newfile` => copy oldfile to newfile

- Renaming a File with **mv**

  `mv oldname newname` => rename oldname to newname

- Removing a File with **rm**

  `rm fileName` => remove the file

- Removing a Directory with **rmdir**

  `rmdir directoryName` => remove the **empty** directory

- Searching with **locate**

  `locate aircrack-ng` => go through your entire filesystem and locate every occurrence of that word.

- Finding Binaries with **whereis**

  `whereis aircrack-ng` => return location of binary file, also return its source and man page if they are available.

- Finding Binaries in the PATH Variable with **which**

  `which aircrack-ng` => return the location of the binaries in the PATH variable in Linux.

- Filtering with **grep**

  The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern

  `grep "localhost" /etc/hosts` => return "localhost" if exists on the file

  we can use it for filtering by piping it to another command ex:

  `ls -l | grep "root"` => return the contents that contain "root"

- Display information about processes running on the
  machine with **ps**

  `ps aux` => list running processes

---

# Chapter #2

> This chapter will teach you how to manipulate text to find, examine, and alter software and files. <br/> In this chapter, we will use several commands and techniques for manipulating text in Linux.

## Commands

- **Taking the Head :** view the beginning of a file. By default, this command ( `head` ) displays the first 10 lines of a file. <br/>
  ex:- `head file.txt` <br/>
  If you want to see more or fewer than the default 10 lines, enter the quantity you want with the dash (-) switch after the call to `head` and before the filename. <br/>
  ex:- `head -5 file.txt`

- **Grabbing That Tail :** The `tail` command is similar to the `head` command, but it’s used to view the last lines of a file. <br/>
  ex:- `tail file.txt`

- **Numbering the Lines :** To display a file with line numbers, we use the `nl` (number lines) command. <br/>
  ex:- `nl file.txt`

- **FILTERING TEXT WITH _GREP_ :** The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern <br/>
  ex:- `ps aux | grep -i "apache"`

- **USING SED TO FIND AND REPLACE :** The sedcommand lets you search for occurrences of a word or a text pattern and then perform some action on it.

  1. Find a word and replace it with a new one and save the result in a new file <br/>
     ex:- `sed s/oldWord/newWord/g searchedFileName > newFileName`

  2. Find a word and replace it on the same file <br/>
     ex:- `sed -i s/oldWord/newWord/g searchFileName`

- **Controlling the Display with _more_ :** The `more` command displays a page of a file at a time and lets you page down through it using the ENTER key. <br/>
  ex:- `more fileName`

- **Displaying and Filtering with _less_ :** Less is a command line utility that displays the contents of a file or a command output, one page at a time. It is similar to more, but has more advanced features and allows you to search and navigate both forward and backward through the file. <br/>
  ex:- `ps aux | less`

---

# Chapter #3

> This chapter will teach you how to manage networks. You’ll scan for networks, find information on connections, and disguise yourself by masking your network and DNS information.

## Commands

- **ANALYZING NETWORKS WITH IFCONFIG :** `ifconfig` stands for "interface configuration." It is used to view and change the configuration of the network interfaces on your system.

  ex: `ifconfig` => displays information about all network interfaces currently in operation

  ex: `sudo ifconfig wlan0 69.72.169.1` => assign a static IP address to an interface, specify the interface name and the IP address

- **CHECKING WIRELESS NETWORK DEVICES WITH IWCONFIG :** `iwconfig` is similar to ifconfig, but is dedicated to the wireless interfaces. It is used to set the parameters of the network interface that are specific to the wireless operation (the wireless frequency, for example). `iwconfig` may also be used to display those parameters, and the wireless statistics

  ex: `iwconfig`

- **Assigning New IP Addresses from the DHCP Server :** The DHCP protocol allows a host to contact a central server which maintains a list of IP addresses which may be assigned on one or more subnets. A DHCP client may request an address from this pool, and then use it on a temporary basis for communication on network. The DHCP protocol also provides a mechanism whereby a client can learn important details about the network to which it is attached, such as the location of a default router, the location of a name server, etc.

  ex: `dhclient eth0`

- **Examining DNS with dig :** The `dig` command in Linux is used to gather DNS information. It stands for Domain Information Groper, and it collects data about Domain Name Servers. The `dig` command is helpful for diagnosing DNS problems, but is also used to display DNS information.

  ex: `dig www.cisco.com`

- **Changing Your DNS Server :** In some cases, you may want to use another DNS server. To do so, you’ll edit a plaintext
  file named `/etc/resolv.conf` on the system. Open that file in a text editor. Then, on your command line, enter the precise name of your editor followed by the location of the file and the filename.

  ex: `sudo nano /etc/resolv.conf` < Then change name server for google name server change it to `8.8.8.8` & `8.8.4.4` >

  **TO KNOW**: *The most common Linux DNS server is the Berkeley Internet Name Domain (BIND).*

- **Mapping Your Own IP Addresses :** A special file on your system called the hosts file also performs domain name–IP
  address translation. The hosts file is located at `/etc/hosts`, and kind of as with DNS, you
  can use it to specify your own IP address–domain name mapping. In other words, you
  can determine which IP address your browser goes to when you enter

  ex: `sudo nano /etc/hosts` < Then add your own IP address >

---
