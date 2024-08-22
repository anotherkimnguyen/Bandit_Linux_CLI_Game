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
## Level 12-13 - :warning: Super difficult
**:computer:Command:**
```sh
bandit12@bandit:~$ mkdir /tmp/kim
bandit12@bandit:~$ cp data.txt /tmp/kim
bandit12@bandit:~$ cd /tmp/kim
bandit12@bandit:/tmp/kim$ ls
[We see we only have one file called data.txt. Let’s decompress using xxd]
bandit12@bandit:/tmp/kim$ xxd -r data.txt > data
bandit12@bandit:/tmp/kim$ ls
[We see we now have data  data.txt]
bandit12@bandit:/tmp/kim$ file data [To see what type of file data is]
[The info we get is that data is gzip compressed and used to be called data2.bin. We need to change the extension to decompress]
bandit12@bandit:/tmp/kim$ mv data file.gz [Changing extension to gz - changing name from data to file too]
bandit12@bandit:/tmp/kim$ gzip -d file.gz [Decompressing]
bandit12@bandit:/tmp/kim$ file file
[file: bzip2 compressed data - let’s change the extension again in order to decompress]
bandit12@bandit:/tmp/kim$ mv file file.bz2
bandit12@bandit:/tmp/kim$ bzip2 -d file.bz2
bandit12@bandit:/tmp/kim$ ls
[We see data.txt and file]
bandit12@bandit:/tmp/kim$ file file
[file: gzip compressed data, was "data4.bin" - let’s change the extension again and decompress and see the type of file and repeat]
bandit12@bandit:/tmp/kim$ mv file file.gz
bandit12@bandit:/tmp/kim$ gzip -d file.gz
bandit12@bandit:/tmp/kim$ ls
[data.txt  file]
bandit12@bandit:/tmp/kim$ file file
[file: POSIX tar archive (GNU) - it’s not gzip or bzip2 compressed, it’s a compressed tar archive. Let’s change the extension to decompress]
bandit12@bandit:/tmp/kim$ mv file file.tar
bandit12@bandit:/tmp/kim$ tar xf file.tar
bandit12@bandit:/tmp/kim$ ls
[Now we have data5.bin  data.txt  file.tar. What type is data5.bin]
bandit12@bandit:/tmp/kim$ file data5.bin
[data5.bin is also a compressed tar archive]
bandit12@bandit:/tmp/kim$ rm file.tar
bandit12@bandit:/tmp/kim$ rm data.txt [Let’s delete those, we’re not using them]
bandit12@bandit:/tmp/kim$ ls
[Now we only have data5.bin]
bandit12@bandit:/tmp/kim$ file data5.bin
[data5.bin: POSIX tar archive (GNU)]
bandit12@bandit:/tmp/kim$ mv data5.bin data.tar [Repeat - list, get type, change extension, decompress, list…]
bandit12@bandit:/tmp/kim$ tar xf data.tar
bandit12@bandit:/tmp/kim$ ls
[data6.bin  data.tar]
bandit12@bandit:/tmp/kim$ file data6.bin
[data6.bin: bzip2 compressed data, block size = 900k]
bandit12@bandit:/tmp/kim$ mv data6.bin data.bz2
bandit12@bandit:/tmp/kim$ bzip2 -d data.bz2
bandit12@bandit:/tmp/kim$ ls
[data  data.tar]
bandit12@bandit:/tmp/kim$ file data
[data: POSIX tar archive (GNU)]
bandit12@bandit:/tmp/kim$ mv data data.tar
bandit12@bandit:/tmp/kim$ tar xf data.tar
bandit12@bandit:/tmp/kim$ ls
[data8.bin  data.tar]
bandit12@bandit:/tmp/kim$ file data8.bin
[data8.bin: gzip compressed data, was "data9.bin"]
bandit12@bandit:/tmp/kim$ mv data8.bin data.gz
bandit12@bandit:/tmp/kim$ gzip -d data.gz
bandit12@bandit:/tmp/kim$ ls
[data  data.tar]
bandit12@bandit:/tmp/kim$ file data
[data: ASCII text - Finally readable!]
bandit12@bandit:/tmp/kim$ cat data
```
Basically, decompress data.txt to data using xxd. See what type of file we have. Change extension to decompress again. List. See what type of file. Change extention to decompress. Repeat :skull:

**:unlock:Password:**

```sh
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
## Level 13-14
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 14-15
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 15-16
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 16-17
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
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
