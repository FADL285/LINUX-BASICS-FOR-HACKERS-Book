# Chapter 6 Exercise Problems

### 1.

Run the `ps` command with the `aux` options on your system and note which process is first and which is last.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  ps aux

USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.9 168076  6616 ?        Ss   08:34   0:05 /sbin/in
root           2  0.0  0.0      0     0 ?        S    08:34   0:00 [kthread
root           3  0.0  0.0      0     0 ?        I<   08:34   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   08:34   0:00 [rcu_par
root           6  0.0  0.0      0     0 ?        I<   08:34   0:00 [kworker
root           9  0.0  0.0      0     0 ?        I<   08:34   0:00 [mm_perc
root          10  0.0  0.0      0     0 ?        S    08:34   0:01 [ksoftir
root          11  0.0  0.0      0     0 ?        I    08:34   0:01 [rcu_sch
root          12  0.0  0.0      0     0 ?        S    08:34   0:00 [migrati
root          13  0.0  0.0      0     0 ?        S    08:34   0:00 [cpuhp/0
root          15  0.0  0.0      0     0 ?        S    08:34   0:00 [kdevtmp
root          16  0.0  0.0      0     0 ?        I<   08:34   0:00 [netns]
root          17  0.0  0.0      0     0 ?        S    08:34   0:00 [kauditd
root          18  0.0  0.0      0     0 ?        S    08:34   0:00 [khungta
root          19  0.0  0.0      0     0 ?        S    08:34   0:00 [oom_rea
root          20  0.0  0.0      0     0 ?        I<   08:34   0:00 [writeba
root          21  0.0  0.0      0     0 ?        S    08:34   0:00 [kcompac
root          22  0.0  0.0      0     0 ?        SN   08:34   0:00 [ksmd]
root          23  0.0  0.0      0     0 ?        SN   08:34   0:00 [khugepa
root          41  0.0  0.0      0     0 ?        I<   08:34   0:00 [kintegr
root          42  0.0  0.0      0     0 ?        I<   08:34   0:00 [kblockd
root          43  0.0  0.0      0     0 ?        I<   08:34   0:00 [blkcg_p
root          44  0.0  0.0      0     0 ?        I<   08:34   0:00 [edac-po
root          45  0.0  0.0      0     0 ?        I<   08:34   0:00 [devfreq
root          46  0.0  0.0      0     0 ?        S    08:34   0:03 [kswapd0
root          47  0.0  0.0      0     0 ?        I<   08:34   0:00 [kthrotl
root          48  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/24-
root          49  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/25-
root          50  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/26-
root          51  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/27-
root          52  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/28-
root          53  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/29-
root          54  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/30-
root          55  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/31-
root          56  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/32-
root          57  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/33-
root          58  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/34-
root          59  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/35-
root          60  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/36-
root          61  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/37-
root          62  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/38-
root          63  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/39-
root          64  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/40-
root          65  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/41-
root          66  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/42-
root          67  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/43-
root          68  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/44-
root          69  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/45-
root          70  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/46-
root          71  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/47-
root          72  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/48-
root          73  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/49-
root          74  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/50-
root          75  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/51-
root          76  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/52-
root          77  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/53-
root          78  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/54-
root          79  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/55-
root          80  0.0  0.0      0     0 ?        I<   08:34   0:00 [acpi_th
root          81  0.0  0.0      0     0 ?        I<   08:34   0:00 [ipv6_ad
root          91  0.0  0.0      0     0 ?        I<   08:34   0:00 [kstrp]
root          94  0.0  0.0      0     0 ?        I<   08:34   0:00 [zswap-s
root          95  0.0  0.0      0     0 ?        I<   08:34   0:00 [kworker
root         133  0.0  0.0      0     0 ?        I<   08:34   0:00 [mpt_pol
root         134  0.0  0.0      0     0 ?        I<   08:34   0:00 [mpt/0]
root         135  0.0  0.0      0     0 ?        I<   08:34   0:00 [ata_sff
root         136  0.0  0.0      0     0 ?        S    08:34   0:00 [scsi_eh
root         137  0.0  0.0      0     0 ?        I<   08:34   0:00 [scsi_tm
root         138  0.0  0.0      0     0 ?        S    08:34   0:00 [irq/16-
root         139  0.0  0.0      0     0 ?        S    08:34   0:00 [scsi_eh
root         140  0.0  0.0      0     0 ?        I<   08:34   0:00 [ttm_swa
root         141  0.0  0.0      0     0 ?        I<   08:34   0:00 [scsi_tm
root         143  0.0  0.0      0     0 ?        I<   08:34   0:00 [cryptd]
root         171  0.0  0.0      0     0 ?        I<   08:34   0:04 [kworker
root         194  0.0  0.0      0     0 ?        S    08:34   0:00 [scsi_eh
root         196  0.0  0.0      0     0 ?        I<   08:34   0:00 [scsi_tm
root         242  0.0  0.0      0     0 ?        S    08:34   0:00 [jbd2/sd
root         243  0.0  0.0      0     0 ?        I<   08:34   0:00 [ext4-rs
root         286  0.0  1.9  60712 14148 ?        Ss   08:34   0:02 /lib/sys
root         293  0.0  0.0      0     0 ?        I<   08:34   0:00 [rpciod]
root         294  0.0  0.0      0     0 ?        I<   08:34   0:00 [xprtiod
root         305  0.0  0.0 150472    40 ?        Ssl  08:34   0:00 vmware-v
root         312  0.0  0.2  22772  1944 ?        Ss   08:34   0:00 /lib/sys
root         374  0.0  0.0      0     0 ?        I<   08:34   0:00 [kworker
root         477  0.0  0.1   8120   876 ?        Ss   08:34   0:00 /usr/sbi
root         480  0.1  0.5 163948  4192 ?        Ssl  08:34   0:13 /usr/bin
root         481  0.0  0.1   6616  1120 ?        Ss   08:34   0:00 /usr/sbi
message+     482  0.0  0.3   8800  2332 ?        Ss   08:34   0:02 /usr/bin
root         484  0.1  1.0 253844  7740 ?        Ssl  08:34   0:09 /usr/sbi
root         487  0.0  0.6 235396  4776 ?        Ssl  08:34   0:00 /usr/lib
root         490  0.0  0.0 222712   540 ?        Ssl  08:34   0:00 /usr/sbi
root         492  0.0  0.2  10936  1528 ?        Ss   08:34   0:00 /usr/sbi
root         494  0.0  0.5  18104  4048 ?        Ss   08:34   0:00 /lib/sys
root         512  0.0  0.2 314572  2004 ?        Ssl  08:34   0:00 /usr/sbi
root         518  0.0  0.5 310104  3988 ?        SLsl 08:34   0:00 /usr/sbi
root         573  0.1  6.7 299176 48448 tty7     Ssl+ 08:34   0:12 /usr/lib
root         574  0.0  0.0   5640   640 tty1     Ss+  08:34   0:00 /sbin/ag
rtkit        763  0.0  0.1 153624   936 ?        SNsl 08:34   0:00 /usr/lib
root         806  0.0  0.2 163784  2140 ?        Sl   08:35   0:00 lightdm
m-fadl         811  0.0  0.3  19468  2816 ?        Ss   08:35   0:00 /lib/sys
m-fadl         812  0.0  0.0 103712   340 ?        S    08:35   0:00 (sd-pam)
m-fadl         831  0.0  0.4 638984  3296 ?        S<sl 08:35   0:00 /usr/bin
m-fadl         837  0.0  0.8 276272  5952 ?        Ssl  08:35   0:00 xfce4-se
m-fadl         845  0.0  0.2   8336  2020 ?        Ss   08:35   0:01 /usr/bin
m-fadl         868  0.0  0.0   5924     4 ?        Ss   08:35   0:00 /usr/bin
m-fadl         878  0.0  0.2 309212  1956 ?        Ssl  08:35   0:00 /usr/lib
m-fadl         883  0.0  0.2   8032  2104 ?        S    08:35   0:00 /usr/bin
m-fadl         887  0.0  0.3 229932  2220 ?        Sl   08:35   0:00 /usr/lib
m-fadl         893  0.0  0.3 169712  2600 ?        Sl   08:35   0:00 /usr/lib
m-fadl         899  0.0  0.1  81020   876 ?        SLs  08:35   0:00 /usr/bin
m-fadl         901  0.0  3.0 397164 22188 ?        Sl   08:35   0:02 xfwm4
m-fadl         904  0.0  0.3 236804  2396 ?        Ssl  08:35   0:00 /usr/lib
m-fadl         909  0.0  0.2 379852  1736 ?        Sl   08:35   0:00 /usr/lib
m-fadl         918  0.0  0.9 236676  7104 ?        Ssl  08:35   0:00 xfsettin
m-fadl         919  0.0  2.8 326876 20584 ?        Sl   08:35   0:00 xfce4-pa
root         922  0.0  0.3 246936  2540 ?        Ssl  08:35   0:00 /usr/lib
m-fadl         930  0.0  3.9 323476 28576 ?        Sl   08:35   0:01 /usr/lib
m-fadl         937  0.0  0.9 201792  6880 ?        Sl   08:35   0:01 /usr/lib
m-fadl         939  0.0  1.0 349364  7296 ?        Sl   08:35   0:00 /usr/lib
m-fadl         940  0.0  1.1 515756  8116 ?        Sl   08:35   0:06 /usr/lib
m-fadl         942  0.0  1.1 247940  8228 ?        Sl   08:35   0:00 /usr/lib
m-fadl         943  0.0  0.9 248040  6596 ?        Sl   08:35   0:00 /usr/lib
m-fadl         945  0.0  1.1 247724  7996 ?        Sl   08:35   0:00 /usr/lib
m-fadl         965  0.0  0.5 350452  3900 ?        Sl   08:35   0:00 Thunar -
m-fadl         971  0.0  2.1 320892 15536 ?        Ssl  08:35   0:03 /usr/lib
m-fadl         978  0.0  3.1 334580 22800 ?        Sl   08:35   0:00 xfdeskto
m-fadl         981  0.0  0.1 233964   820 ?        Sl   08:35   0:00 /usr/lib
m-fadl         982  0.0  0.4 244712  3124 ?        Sl   08:35   0:00 xiccd
m-fadl         988  0.0  1.5 441352 11448 ?        Sl   08:35   0:00 /usr/bin
m-fadl         996  0.1  1.6 294388 12040 ?        Sl   08:35   0:14 /usr/bin
colord       997  0.0  0.3 244312  2308 ?        Ssl  08:35   0:00 /usr/lib
m-fadl         999  0.0  0.0  20792   468 ?        Ssl  08:35   0:00 xcape -e
m-fadl        1003  0.0  0.3 193396  2332 ?        Sl   08:35   0:00 /usr/lib
m-fadl        1007  0.0  1.4 271664 10716 ?        Sl   08:35   0:00 light-lo
m-fadl        1013  0.0  0.0 155816   520 ?        Sl   08:35   0:00 /usr/lib
m-fadl        1014  0.0  1.6 402604 12064 ?        Sl   08:35   0:04 nm-apple
m-fadl        1030  0.0  0.5 198480  3928 ?        Ssl  08:35   0:00 xfce4-po
m-fadl        1043  0.0  5.4 412548 39232 ?        Sl   08:35   0:05 /usr/bin
m-fadl        1065  0.0  0.6   8704  4836 pts/0    Ss   08:35   0:00 /bin/bas
m-fadl        1076  0.0  2.7 288652 19496 ?        Sl   08:35   0:00 /usr/bin
m-fadl        1077  0.0  0.1  44916   872 ?        Ss   08:35   0:00 /usr/lib
m-fadl        1086  0.0  0.4 348748  3332 ?        Ssl  08:35   0:00 /usr/lib
root        1089  0.0  0.4 393396  3204 ?        Ssl  08:35   0:00 /usr/lib
m-fadl        1103  0.0  0.6 311448  4416 ?        Ssl  08:35   0:00 /usr/lib
m-fadl        1108  0.0  0.2 232796  1968 ?        Ssl  08:35   0:00 /usr/lib
m-fadl        1112  0.0  0.2 232996  1888 ?        Ssl  08:35   0:00 /usr/lib
m-fadl        1116  0.0  0.3 235168  2328 ?        Ssl  08:35   0:00 /usr/lib
m-fadl        1123  0.0  0.2 310912  1644 ?        Sl   08:35   0:00 /usr/lib
m-fadl        1128  0.0  0.2 159244  1844 ?        Ssl  08:35   0:00 /usr/lib
root        4145  0.2  0.0      0     0 ?        I    08:51   0:19 [kworker
root        9544  0.2  0.0      0     0 ?        I    10:19   0:04 [kworker
root        9617  0.0  0.0      0     0 ?        I    10:23   0:00 [kworker
lightdm    10462  0.0  1.2  19456  8744 ?        Ss   10:38   0:00 /lib/sys
lightdm    10463  0.0  0.3 169248  2180 ?        S    10:38   0:00 (sd-pam)
lightdm    10486  0.0  0.5   7896  3940 ?        Ss   10:38   0:00 /usr/bin
lightdm    10487  0.0  0.7 309068  5620 ?        Ssl  10:38   0:00 /usr/lib
lightdm    10492  0.0  0.5   7764  3800 ?        S    10:38   0:00 /usr/bin
lightdm    10494  0.0  1.0 236808  7264 ?        Ssl  10:38   0:00 /usr/lib
lightdm    10499  0.0  0.8 379852  6384 ?        Sl   10:38   0:00 /usr/lib
lightdm    10522  0.0  0.9 169572  6888 ?        Sl   10:38   0:00 /usr/lib
root       10579  0.0  0.0      0     0 ?        I    10:45   0:00 [kworker
root       10581  0.0  0.0      0     0 ?        I    10:46   0:00 [kworker
root       10583  0.0  0.0      0     0 ?        I    10:51   0:00 [kworker
m-fadl       10589  0.0  0.4   9572  3300 pts/0    R+   10:52   0:00 ps aux
```

---

### 2.

Run the `top` command and note the two processes using the greatest amount of your resources.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  top

PID   USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+
10608 root      20   0  283688  69696  35556 S   2.3   9.7   0:00.74
10883 m-fadl      20   0  405052  80472  63216 S   2.3  11.1   0:00.43
10738 m-fadl      20   0  397176  81924  56572 S   0.7  11.3   0:00.32
9544  root      20   0       0      0      0 I   0.3   0.0   0:05.87
10760 m-fadl      20   0  515760  35652  28340 S   0.3   4.9   0:00.12
```

---

### 3.

Use the `kill` command to kill the process that uses the most resources.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  kill 10883
```

---

### 4.

Use the `renice` command to reduce the priority of a running process to `+19`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  renice 19 10902

10902 (process ID) old priority 0, new priority 19
```

---

### 5.

Create a script called `myscanning` (to see how to write a bash script, see Chapter 8; the content of the script is not important) with a text editor and then schedule it to run next Wednesday at `1 AM`.

---

```shell
┌──(m-fadl㉿Fadl)-[~]
└─$  at 1:00am 09/09/2020

warning: commands will be executed using /bin/sh
at> /home/m-fadl/myscanning
at> <EOT>
job 1 at Wed Sep  9 01:00:00 2020
```

---
