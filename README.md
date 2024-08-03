# Over the wire _ Bandit
---
#### level 0:
```
─$ ssh bandit0@bandit.labs.overthewire.org -p2220
```
```
password :bandit0
```
```
bandit0@bandit:~$ ls
bandit0@bandit:~$ cat readme
```
#### level 1:
```
─$ ssh bandit1@bandit.labs.overthewire.org -p2220
```
```
password : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```
```
bandit1@bandit:~$ ls
bandit1@bandit:~$ cat ./-
```
#### level 2:
```
─$ ssh bandit2@bandit.labs.overthewire.org -p2220
```
```
password : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```
```
bandit2@bandit:~$ ls
bandit2@bandit:~$ cat "spaces in this filename"
```
#### level 3:
```
─$ ssh bandit3@bandit.labs.overthewire.org -p2220
```
```
password : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You 
```
#### level 4:
```
─$ ssh bandit4@bandit.labs.overthewire.org -p2220
```
```
password : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
```
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
bandit4@bandit:~/inhere$ file ./-file0*
bandit4@bandit:~/inhere$ cat ./-file07
```
#### level 5:
```
─$ ssh bandit5@bandit.labs.overthewire.org -p2220
```
```
password : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
bandit5@bandit:~/inhere$ find . -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
```
#### level 6:
```
─$ ssh bandit6@bandit.labs.overthewire.org -p2220
```
```
password : HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
```
bandit6@bandit:~$ find  / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
```
#### level 7:
```
─$ ssh bandit7@bandit.labs.overthewire.org -p2220
```
```
password : morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep millionth
```
#### level 8:
```
─$ ssh bandit8@bandit.labs.overthewire.org -p2220
```
```
password : dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
```
#### level 9:
```
─$ ssh bandit9@bandit.labs.overthewire.org -p2220
```
```
password : 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```
```
bandit9@bandit:~$ strings data.txt | grep "="
```
#### level 10:
```
─$ ssh bandit10@bandit.labs.overthewire.org -p2220
```
```
password : FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ cat data.txt | base64 --decode
```
#### level 11:
```
─$ ssh bandit11@bandit.labs.overthewire.org -p2220
```
```
password : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
```