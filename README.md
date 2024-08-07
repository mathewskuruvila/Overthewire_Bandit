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

#### level 12:
```
─$ ssh bandit12@bandit.labs.overthewire.org -p2220
```
```
password : 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```
```
bandit12@bandit:~$ mkdir /tmp/xyz
bandit12@bandit:~$ cp data.txt /tmp/xyz
bandit12@bandit:~$ cd /tmp/xyz
bandit12@bandit:/tmp/xyz$ ls
data.txt
bandit12@bandit:/tmp/xyz$ xxd -r data.txt > data_xxd_reverse

bandit12@bandit:/tmp/xyz$ file data_xxd_reverse
data_xxd_reverse: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix

bandit12@bandit:/tmp/xyz$ zcat data_xxd_reverse > data_zcat
bandit12@bandit:/tmp/xyz$ file data_zcat
data_zcat: bzip2 compressed data, block size = 900k

bandit12@bandit:/tmp/xyz$ bzip2 -d data_zcat
bzip2: Can't guess original name for data_zcat -- using data_zcat.out
bandit12@bandit:/tmp/xyz$ file data_zcat.out
data_zcat.out: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix

bandit12@bandit:/tmp/xyz$ zcat data_zcat.out > data_zcat_2
bandit12@bandit:/tmp/xyz$ file data_zcat_2
data_zcat_2: POSIX tar archive (GNU)

bandit12@bandit:/tmp/xyz$ tar -xvf data_zcat_2
data5.bin
bandit12@bandit:/tmp/xyz$ file data5.bin
data5.bin: POSIX tar archive (GNU)

bandit12@bandit:/tmp/xyz$ tar -xvf data5.bin
data6.bin
bandit12@bandit:/tmp/xyz$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k

bandit12@bandit:/tmp/xyz$ bzip2 -d data6.bin
bzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/xyz$ file data6.bin.out
data6.bin.out: POSIX tar archive (GNU)

bandit12@bandit:/tmp/xyz$ tar -xvf data6.bin.out
data8.bin
bandit12@bandit:/tmp/xyz$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix

bandit12@bandit:/tmp/xyz$ zcat data8.bin

```
#### Key Takeaways
gzip decompress

$ zcat in_file > out_file

bzip2 decompress

$ bzip2 -d file

tar decompress

$ tar xvf file

#### level 13:

```
─$ ssh bandit13@bandit.labs.overthewire.org -p2220
```
```
password : FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
```
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ file sshkey.private
sshkey.private: PEM RSA private key
bandit13@bandit:~$ cat sshkey.private 
bandit13@bandit:~$ ssh bandit14@localhost -i sshkey.private -p 2220
```
#### level 14:
```
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
#### level 15:
```
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS                                
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```