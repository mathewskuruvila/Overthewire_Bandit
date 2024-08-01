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