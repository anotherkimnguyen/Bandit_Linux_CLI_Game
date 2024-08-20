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
~$ cd inhere
~inhere$ ls -a

There's a file called "...Hiding-From-You"

~inhere$ cat ...Hiding-From-You

```

**:unlock:Password:**

```sh
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

## Level 4-5
**:computer:Command:**

```sh
~$ cd inhere
~inhere$ ls

Shows a bunch of files named -fileDIGITS

~inhere$ file ./-file* 

Shows that file07 is ASCII text

~inhere$ cat ./-file07
```

**:unlock:Password:**

```sh
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

## Level 5-6
**:computer:Command:**

```sh
~$ cd inhere
~inhere$ find . -type f -size 1033c ! -executable (it's a file, it's 1033 bytes in size and it's not executable)
~inhere$ cat ./maybehere07/.file2
```

**:unlock:Password:**

```sh
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
## Level 6-7
**:computer:Command:**

```sh
~$ find / -user bandit7 -group bandit6 -size 33c

A bunch of "Permission denied" messages

~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null to suppress error messages about directories I don't have access to

Shows a file called "/var/lib/dpkg/info/bandit7.password"

~$ cat /var/lib/dpkg/info/bandit7.password
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
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 10-11
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 11-12
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
```
## Level 12-13
**:computer:Command:**
```sh
xx
```
**:unlock:Password:**

```sh
XXX
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