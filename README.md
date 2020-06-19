[<img src="https://avatars2.githubusercontent.com/u/24763891?s=400&u=c1150e7da5667f47159d433d8e49dad99a364f5f&v=4"  width="256px" height="256px" align="right" alt="Multiverse OS Logo">](https://github.com/multiverse-os)

## Multiverse: Core Utilities 
**URL** [multiverse-os.org](https://multiverse-os.org)

The focus on re-imagining the `GNU core-utils` is one feature of Multiverse OS  
sets it apart from many other Linux distributions. After discussing the topic
with many novice users, we have discovered that the lack of consistency between
the core utilities is a commonly reported problem people had learning Linux.

Multiverse OS is designed specifically to make Linux more approachable; focusing
on making it easier to learn, but also faster to learn, so that time invested in
learning is productive as possible. 

The primary aspects of the Multiverse OS core utilities that sets it apart from
other Linux distributions are: 

  * **Consistency** because many of the commands were developed by volunteers
    building commands they thought would be useful, and so there was little
    coordination between development teams. Meaning some command recursive flag
    is `-r` and others is `-R`. This can make learning the console much more
    difficult than it needs to be, and by making these flags consistent allows
    new users to take what they learn with one command, and apply it immediately
    to another, speeding up the learning process.

  * **Removal of concept of local vs remote hosts** at the time of writing the
    original command the concept of remote and local hosts were dramatic, but
    with Multiverse OS, and all the nested virtual machines within a cluster,
    this distiction is blurred. To simplify the number of commands to learn, we
    merge together commands like `cp` and `scp` for simplicity, and consistency.

  * **Removal of concept of ipv4 vs ipv6 addresses** due to the migration from
    ipv4 and ipv6 occuring over a long period of time to make it easier for
    administrators before and after this divide, simple commands like ping and
    other network commands have an ipv4 and ipv6 versions. These are merged
    together to remove any unncessary complexity. 

  * **Every command has a library** to make working with the tools easy. No
    longer will your software need a long string of commands to cut-up and parse
    out the output of one command to get data from commands. This makes software
    more secure too because there is less opportunity for breaking out of
    console command, to run arbitrary commands. Instead by directly interacting
    with the library, we remove this security issue, and make it easier for
    developers to build new tools. 

  * **Every command has JSON/XML** output for easier scripting, with reduced
    complexity. 

  * **Full localisation** from the command name, to the output; every aspect of
    each of the core utilities is translated and therefore even the lowest
    levels of the system is accessible to an international community. 


And for maximum compatibility, a shim exists to ensure that all legacy commands
continue to work via a shim; so that new users can learn the new system, but
still use answers from the internet for older style commands; and existing Linux
users can use Multiverse OS without issue, learning the new commands if they
desire and at their own pace. 

#### Development 
Currently, we are collecting basic versions of each command, that provide the
conventional functionality. Then we will start building the Multiverse OS
alternative. This will allow for the creation of a better shim system. The
Multiverse OS defeault command list will be based off the Debian defaults, and
built around the functionality provided by default Debian installation. 

### Debian Packages 
The packages Multiverse OS core utilities will cover will cover the
functionality supplied by the following packages (the scope may be reduced, and
several to many commands may be merged into a single command for greater
simplicity): 

  * [`coreutils` package](https://packages.debian.org/bullseye/amd64/coreutils/filelist) 
  
```
/bin/cat
/bin/chgrp
/bin/chmod
/bin/chown
/bin/cp
/bin/date
/bin/dd
/bin/df
/bin/dir
/bin/echo
/bin/false
/bin/ln
/bin/ls
/bin/mkdir
/bin/mknod
/bin/mktemp
/bin/mv
/bin/pwd
/bin/readlink
/bin/rm
/bin/rmdir
/bin/sleep
/bin/stty
/bin/sync
/bin/touch
/bin/true
/bin/uname
/bin/vdir
/usr/bin/arch
/usr/bin/b2sum
/usr/bin/base32
/usr/bin/base64
/usr/bin/basename
/usr/bin/chcon
/usr/bin/cksum
/usr/bin/comm
/usr/bin/csplit
/usr/bin/cut
/usr/bin/dircolors
/usr/bin/dirname
/usr/bin/du
/usr/bin/env
/usr/bin/expand
/usr/bin/expr
/usr/bin/factor
/usr/bin/fmt
/usr/bin/fold
/usr/bin/groups
/usr/bin/head
/usr/bin/hostid
/usr/bin/id
/usr/bin/install
/usr/bin/join
/usr/bin/link
/usr/bin/logname
/usr/bin/md5sum
/usr/bin/md5sum.textutils
/usr/bin/mkfifo
/usr/bin/nice
/usr/bin/nl
/usr/bin/nohup
/usr/bin/nproc
/usr/bin/numfmt
/usr/bin/od
/usr/bin/paste
/usr/bin/pathchk
/usr/bin/pinky
/usr/bin/pr
/usr/bin/printenv
/usr/bin/printf
/usr/bin/ptx
/usr/bin/realpath
/usr/bin/runcon
/usr/bin/seq
/usr/bin/sha1sum
/usr/bin/sha224sum
/usr/bin/sha256sum
/usr/bin/sha384sum
/usr/bin/sha512sum
/usr/bin/shred
/usr/bin/shuf
/usr/bin/sort
/usr/bin/split
/usr/bin/stat
/usr/bin/stdbuf
/usr/bin/sum
/usr/bin/tac
/usr/bin/tail
/usr/bin/tee
/usr/bin/test
/usr/bin/timeout
/usr/bin/tr
/usr/bin/truncate
/usr/bin/tsort
/usr/bin/tty
/usr/bin/unexpand
/usr/bin/uniq
/usr/bin/unlink
/usr/bin/users
/usr/bin/wc
/usr/bin/who
/usr/bin/whoami
/usr/bin/yes
/usr/sbin/chroot
``` 

  * [`netutils` package](https://packages.debian.org/sid/alpha/net-tools/filelist) 

```
/bin/netstat
/sbin/ifconfig
/sbin/ipmaddr
/sbin/iptunnel
/sbin/mii-tool
/sbin/nameif
/sbin/plipconfig
/sbin/rarp
/sbin/route
/sbin/slattach
/usr/sbin/arp 
``` 

  * [`util-linux` package](https://packages.debian.org/bullseye/amd64/util-linux/filelist)

```
/bin/dmesg
/bin/findmnt
/bin/lsblk
/bin/more
/bin/mountpoint
/bin/su
/bin/wdctl
/sbin/agetty
/sbin/blkdiscard
/sbin/blkid
/sbin/blkzone
/sbin/blockdev
/sbin/chcpu
/sbin/ctrlaltdel
/sbin/findfs
/sbin/fsck
/sbin/fsck.cramfs
/sbin/fsck.minix
/sbin/fsfreeze
/sbin/fstrim
/sbin/getty
/sbin/hwclock
/sbin/isosize
/sbin/mkfs
/sbin/mkfs.bfs
/sbin/mkfs.cramfs
/sbin/mkfs.minix
/sbin/mkswap
/sbin/pivot_root
/sbin/raw
/sbin/runuser
/sbin/sulogin
/sbin/swaplabel
/sbin/switch_root
/sbin/wipefs
/sbin/zramctl
/usr/bin/addpart
/usr/bin/choom
/usr/bin/chrt
/usr/bin/delpart
/usr/bin/fallocate
/usr/bin/fincore
/usr/bin/flock
/usr/bin/getopt
/usr/bin/i386
/usr/bin/ionice
/usr/bin/ipcmk
/usr/bin/ipcrm
/usr/bin/ipcs
/usr/bin/last
/usr/bin/lastb
/usr/bin/linux32
/usr/bin/linux64
/usr/bin/lscpu
/usr/bin/lsipc
/usr/bin/lslocks
/usr/bin/lslogins
/usr/bin/lsmem
/usr/bin/lsns
/usr/bin/mcookie
/usr/bin/mesg
/usr/bin/namei
/usr/bin/nsenter
/usr/bin/partx
/usr/bin/prlimit
/usr/bin/rename.ul
/usr/bin/resizepart
/usr/bin/rev
/usr/bin/setarch
/usr/bin/setpriv
/usr/bin/setsid
/usr/bin/setterm
/usr/bin/taskset
/usr/bin/unshare
/usr/bin/utmpdump
/usr/bin/whereis
/usr/bin/x86_64
/usr/sbin/chmem
/usr/sbin/fdformat
/usr/sbin/ldattach
/usr/sbin/readprofile
/usr/sbin/rtcwake
```


