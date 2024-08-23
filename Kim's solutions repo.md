# Solution for clmystery - [Game here](https://github.com/veltman/clmystery)
The murderer is ***Jeremy Bowers*** 💀
# Passwords for the Trial of Might/Bandit game - [Game here](https://overthewire.org/wargames/bandit/)
## Level 0-1
**:computer:Command:**

```sh
cat readme
```

**:unlock:Password:**

```sh
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

## Level 1-2
**:computer:Command:**

```sh
cat < - 
```

**:unlock:Password:**

```sh
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

## Level 2-3
**:computer:Command:**

```sh
cat "spaces in this filename"
```

**:unlock:Password:**

```sh
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

## Level 3-4
**:computer:Command:**

```sh
cd inhere
ls -a
(There's a file called "...Hiding-From-You")
cat ...Hiding-From-You
```

**:unlock:Password:**

```sh
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

## Level 4-5
**:computer:Command:**

```sh
cd inhere
ls
(Shows a bunch of files named -fileDIGITS)
file ./-file* 
(Shows that file07 is ASCII text)
cat ./-file07
```

**:unlock:Password:**

```sh
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

## Level 5-6
**:computer:Command:**

```sh
cd inhere
find . -type f -size 1033c ! -executable (it's a file, it's 1033 bytes in size and it's not executable)
cat ./maybehere07/.file2
```

**:unlock:Password:**

```sh
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
## Level 6-7
**:computer:Command:**

```sh
find / -user bandit7 -group bandit6 -size 33c
(A bunch of "Permission denied" messages)
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null (to suppress error messages about directories I don't have access to)
(Shows a file called "/var/lib/dpkg/info/bandit7.password")
cat /var/lib/dpkg/info/bandit7.password
```

**:unlock:Password:**

```sh
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
## Level 7-8
**:computer:Command:**
```sh
grep millionth data.txt
```
**:unlock:Password:**

```sh
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
## Level 8-9
**:computer:Command:**
```sh
~$ cat data.txt

File is huge

~$ cat data.txt | sort (to sort lines in order)
~$ cat data.txt | sort | uniq -u (I only want the line that appears once)
```
**:unlock:Password:**

```sh
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
## Level 9-10
**:computer:Command:**
```sh
strings data.txt | grep =
or
strings data.txt | grep ^= to only see the lines that begin with =
```
**:unlock:Password:**

```sh
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
## Level 10-11
**:computer:Command:**
```sh
base64 -d data.txt
```
**:unlock:Password:**

```sh
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
## Level 11-12
**:computer:Command:**
```sh
cat data.txt | tr A-Za-z N-ZA-Mn-za-m (translate A-Z and a-z)
```
**:unlock:Password:**

```sh
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
## Level 12-13 :warning:
**:computer:Command:**
```sh
bandit12@bandit:~$ ls
(We see we have data.txt - let's create a directory)
bandit12@bandit:~$ mkdir /tmp/kim
(Let's copy data.txt to our directory)
bandit12@bandit:~$ cp data.txt /tmp/kim
(Let's work in that directory)
bandit12@bandit:~$ cd /tmp/kim
bandit12@bandit:/tmp/kim$ ls
(We do have data.txt - let's reverse the hexdump)
bandit12@bandit:/tmp/kim$ xxd -r data.txt > data
bandit12@bandit:/tmp/kim$ ls
(We now have two files - data  data.txt - we don't need data.txt, let's remove so as not to get confused)
bandit12@bandit:/tmp/kim$ rm data.txt
(We need to get information on data)
bandit12@bandit:/tmp/kim$ file data
(It is gzip compressed data, formerly named "data2.bin")
(Since we know gzip compressed it, we need to use gzip to decompress it)
(So we need to change the extension to .gz)
bandit12@bandit:/tmp/kim$ mv data data.gz
bandit12@bandit:/tmp/kim$ gzip -d data.gz
bandit12@bandit:/tmp/kim$ ls
(we get data)
bandit12@bandit:/tmp/kim$ file data
(data: bzip2 compressed data, block size = 900k)
bandit12@bandit:/tmp/kim$ mv data data.bz2
bandit12@bandit:/tmp/kim$ bzip2 -d data.bz2
bandit12@bandit:/tmp/kim$ ls
(data)
bandit12@bandit:/tmp/kim$ file data
data: gzip compressed data, was "data4.bin"
bandit12@bandit:/tmp/kim$ mv data data.gz
bandit12@bandit:/tmp/kim$ gzip -d data.gz
bandit12@bandit:/tmp/kim$ ls
(data)
bandit12@bandit:/tmp/kim$ file data
(data: POSIX tar archive (GNU))
bandit12@bandit:/tmp/kim$ mv data data.tar
bandit12@bandit:/tmp/kim$ tar xf data.tar
bandit12@bandit:/tmp/kim$ ls
(data5.bin  data.tar)
bandit12@bandit:/tmp/kim$ rm data.tar
bandit12@bandit:/tmp/kim$ file data5.bin
(data5.bin: POSIX tar archive (GNU))
bandit12@bandit:/tmp/kim$ mv data5.bin data.tar
bandit12@bandit:/tmp/kim$ tar xf data.tar
bandit12@bandit:/tmp/kim$ ls
(data6.bin  data.tar)
bandit12@bandit:/tmp/kim$ rm data.tar
bandit12@bandit:/tmp/kim$ file data6.bin
(data6.bin: bzip2 compressed data, block size = 900k)
bandit12@bandit:/tmp/kim$ mv data6.bin data.bz2
bandit12@bandit:/tmp/kim$ bzip2 -d data.bz2
bandit12@bandit:/tmp/kim$ ls
(data)
bandit12@bandit:/tmp/kim$ file data
(data: POSIX tar archive (GNU))
bandit12@bandit:/tmp/kim$ mv data data.tar
bandit12@bandit:/tmp/kim$ tar xf data.tar
bandit12@bandit:/tmp/kim$ ls
(data8.bin  data.tar)
bandit12@bandit:/tmp/kim$ rm data.tar
bandit12@bandit:/tmp/kim$ file data8.bin
(data8.bin: gzip compressed data, was "data9.bin")
bandit12@bandit:/tmp/kim$ mv data8.bin data.gz
bandit12@bandit:/tmp/kim$ gzip -d data.gz
bandit12@bandit:/tmp/kim$ ls
(data)
bandit12@bandit:/tmp/kim$ file data
(data: ASCII text)
bandit12@bandit:/tmp/kim$ cat data
```

**:unlock:Password:**

```sh
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
## Level 13-14
**:computer:Command:**
```sh
ls
(We have sshkey.private - let's use this to enter bandit14)
ssh -i sshkey.private bandit14@localhost -p 2220
cat /etc/bandit_pass/bandit14
```
**:unlock:Password:**

```sh
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
## Level 14-15
**:computer:Command:**
```sh
(Start from bandit14)
nc localhost 30000
```
**:unlock:Password:**

```sh
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
## Level 15-16
**:computer:Command:**
```sh
ncat --ssl localhost 30001 (We hit enter and we enter the previous level's password aka:)
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
(We get:)
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
**:unlock:Password:**

```sh
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
## Level 16-17 :warning:
**:computer:Command:**
```sh
(We need to identify which ports are open)
nmap -p 31000-32000 localhost
(We have 5 open ports - we need to check every port with our current level password)
ncat localhost 31046 < /etc/bandit_pass/bandit16
ncat --ssl localhost 31518 < /etc/bandit_pass/bandit16
ncat localhost 31691 < /etc/bandit_pass/bandit16
ncat --ssl localhost 31790 < /etc/bandit_pass/bandit16
(We get the private key)
(Copy the private key text)
exit
touch pvt.key
nano pvt.key
(Paste key text)
(Make it private)
chmod 700 pvt.key
ssh bandit17@bandit.labs.overthewire.org -i pvt.key -p 2220
```
**:unlock:Password:**

```sh
And now we've entered lvl 17
```
## Level 17-18
**:computer:Command:**
```sh
diff passwords.new passwords.old
42c42
< x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
---
> bSrACvJvvBSxEM2SGsV5sn09vc3xgqyp
```
**:unlock:Password:**

```sh
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```
## Level 18-19
**:computer:Command:**
```sh
(Get into bandit18 without getting Bye bye)
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat ~/readme" (because we know the next password in a readme file)
(Enter password x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO)
(We get cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8)
```
**:unlock:Password:**

```sh
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```
## Level 19-20
**:computer:Command:**
```sh
ls
(We get bandit20-do)
ls -la
(We get:
total 36
drwxr-xr-x  2 root     root      4096 Jul 17 15:57 .
drwxr-xr-x 70 root     root      4096 Jul 17 15:58 ..
-rwsr-x---  1 bandit20 bandit19 14880 Jul 17 15:57 bandit20-do
-rw-r--r--  1 root     root       220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root     root      3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root     root       807 Mar 31 08:41 .profile)
./bandit20-do
(we get Run a command as another user)
bandit19@bandit:~$ ./bandit20-do id
(We get uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19))
bandit19@bandit:~$ ./bandit20-do ls -la /etc/bandit_pass
(We get:
total 152
drwxr-xr-x   2 root     root      4096 Jul 17 15:56 .
drwxr-xr-x 121 root     root     12288 Aug  1 14:49 ..
-r--------   1 bandit0  bandit0      8 Jul 17 15:56 bandit0
-r--------   1 bandit1  bandit1     33 Jul 17 15:56 bandit1
-r--------   1 bandit10 bandit10    33 Jul 17 15:56 bandit10
-r--------   1 bandit11 bandit11    33 Jul 17 15:56 bandit11
-r--------   1 bandit12 bandit12    33 Jul 17 15:56 bandit12
-r--------   1 bandit13 bandit13    33 Jul 17 15:56 bandit13
-r--------   1 bandit14 bandit14    33 Jul 17 15:56 bandit14
-r--------   1 bandit15 bandit15    33 Jul 17 15:56 bandit15
-r--------   1 bandit16 bandit16    33 Jul 17 15:56 bandit16
-r--------   1 bandit17 bandit17    33 Jul 17 15:56 bandit17
-r--------   1 bandit18 bandit18    33 Jul 17 15:56 bandit18
-r--------   1 bandit19 bandit19    33 Jul 17 15:56 bandit19
-r--------   1 bandit2  bandit2     33 Jul 17 15:56 bandit2
-r--------   1 bandit20 bandit20    33 Jul 17 15:56 bandit20
-r--------   1 bandit21 bandit21    33 Jul 17 15:56 bandit21
-r--------   1 bandit22 bandit22    33 Jul 17 15:56 bandit22
-r--------   1 bandit23 bandit23    33 Jul 17 15:56 bandit23
-r--------   1 bandit24 bandit24    33 Jul 17 15:56 bandit24
-r--------   1 bandit25 bandit25    33 Jul 17 15:56 bandit25
-r--------   1 bandit26 bandit26    33 Jul 17 15:56 bandit26
-r--------   1 bandit27 bandit27    33 Jul 17 15:56 bandit27
-r--------   1 bandit28 bandit28    33 Jul 17 15:56 bandit28
-r--------   1 bandit29 bandit29    33 Jul 17 15:56 bandit29
-r--------   1 bandit3  bandit3     33 Jul 17 15:56 bandit3
-r--------   1 bandit30 bandit30    33 Jul 17 15:56 bandit30
-r--------   1 bandit31 bandit31    33 Jul 17 15:56 bandit31
-r--------   1 bandit32 bandit32    33 Jul 17 15:56 bandit32
-r--------   1 bandit33 bandit33    33 Jul 17 15:56 bandit33
-r--------   1 bandit4  bandit4     33 Jul 17 15:56 bandit4
-r--------   1 bandit5  bandit5     33 Jul 17 15:56 bandit5
-r--------   1 bandit6  bandit6     33 Jul 17 15:56 bandit6
-r--------   1 bandit7  bandit7     33 Jul 17 15:56 bandit7
-r--------   1 bandit8  bandit8     33 Jul 17 15:56 bandit8
-r--------   1 bandit9  bandit9     33 Jul 17 15:56 bandit9)
./bandit20-do cat /etc/bandit_pass/bandit20
```
**:unlock:Password:**

```sh
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```
## Level 20-21
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 21-22
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 22-23
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
