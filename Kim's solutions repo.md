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
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 18-19
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 19-20
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
