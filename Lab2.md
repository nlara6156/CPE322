# Lab 2 

### 1

Command: `hostname`

Expected Output: Will print the host name of the system

Output:
```
PS C:\Users\nadia> hostname

DESKTOP-VTE7PSP
```

---

### 2

Command: `env`

Expected Output: Will print the environment variables of the system

Output: 

```
PS C:\Users\nadia> env

... (private)
```

---

### 3

Command: `ps`

Expected Output: Will print the status of active processes

Output:
```
PS C:\Users\nadia> ps

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName
    223      15     3072      12324              2924   0 ae...
    185      12     2868      10936             12236   0 Ag...
    229      20     3256      11860       5.59  21272   1 Ap...
   1066      30    36260      51400       5.50  23792   1 Ap...
    312      32    17876       2200       0.09  20416   1 ba...
```
 etc.

 ---

### 4

Command: `pwd`

Expected Output: Will display the full path to your current directory

Output: 
```
PS C:\Users\nadia> pwd

Path
----
C:\Users\nadia

```

---

### 5

Command: `git clone https://github.com/kevinwlu/iot.git`

Expected Output: Will point to Kevin Lu's iot repository and clone it into my directory

Output:

```
PS C:\Users\nadia> git clone https://github.com/kevinwlu/iot.git

Cloning into 'iot'...
remote: Enumerating objects: 23032, done.
remote: Counting objects: 100% (4081/4081), done.
remote: Compressing objects: 100% (1237/1237), done.
remote: Total 23032 (delta 2323), reused 3981 (delta 2253), pack-reused 18951
Receiving objects: 100% (23032/23032), 28.78 MiB | 7.96 MiB/s, done.
Resolving deltas: 100% (15022/15022), done.
```
---

### 6

Command: `cd iot`

Expected Output: Will change the directory to iot

Output:

```
PS C:\Users\nadia> cd iot
PS C:\Users\nadia\iot>
```

---

### 7

Command: `ls`

Expected Output: Will display the files in the current directory

Output:
```
PS C:\Users\nadia\iot> ls


    Directory: C:\Users\nadia\iot


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         3/27/2024   3:05 PM                apps
d-----         3/27/2024   3:05 PM                cases
d-----         3/27/2024   3:05 PM                economics
d-----         3/27/2024   3:05 PM                health
d-----         3/27/2024   3:05 PM                hype
d-----         3/27/2024   3:05 PM                lesson1
d-----         3/27/2024   3:05 PM                lesson10
d-----         3/27/2024   3:05 PM                lesson2
d-----         3/27/2024   3:05 PM                lesson3
d-----         3/27/2024   3:05 PM                lesson4
d-----         3/27/2024   3:05 PM                lesson5
d-----         3/27/2024   3:05 PM                lesson6
d-----         3/27/2024   3:05 PM                lesson7
d-----         3/27/2024   3:05 PM                lesson8
d-----         3/27/2024   3:05 PM                lesson9
d-----         3/27/2024   3:05 PM                make
d-----         3/27/2024   3:05 PM                projects
d-----         3/27/2024   3:05 PM                special_probl
                                                  ems
d-----         3/27/2024   3:05 PM                standards
d-----         3/27/2024   3:05 PM                systems
d-----         3/27/2024   3:05 PM                tools
-a----         3/27/2024   3:05 PM          17690 README.md
```

---

### 8

Command: `cd`

Expected Output: This will change the directory. The terminal will move into an existing file name you enter following cd on the command line. 

Output:

```
PS C:\Users\nadia> cd Work
PS C:\Users\nadia\Work>
```

---

### 9

Command: `df`

Expected Output: Will display the amount of available disk space

Output:

```
PS C:\Users\nadia\iot> df
Filesystem     1K-blocks      Used Available Use% Mounted on
C:/msys64      482872316 219293932 263578384  46% /
```

---

### 10

Command: `mkdir demo`

Expected Output: The mkdir command allows the user to make new directories in the terminal. 

Output:

```
PS C:\Users\nadia\iot> mkdir demo


    Directory: C:\Users\nadia\iot


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         3/27/2024   3:27 PM                demo
```

---

### 11

Command: `cd demo`

Expected Output: This will change the directory into the demo directory that we created in the previous command.

Output:

```
PS C:\Users\nadia\iot> cd demo
PS C:\Users\nadia\iot\demo>
```

---

### 12

Command: `nano file`

Expected Output: The nano command is used to open, edit, save and exit files quickly. The filename typed following nano is the file that will be opened.

Output:
`will input photo`

---

### 13

Command: `cat file`

Expected Output: The cat, short for concatenate, command allows the terminal to display the contents of one or more files without opening it for editing.

Output: 

```
PS C:\Users\nadia\iot\demo> cat file
CPE 322
```

---

### 14

Command: `cp  file file1`

Expected Output: The cp command copies a file to another location. This will copy 'file' to 'file1'

Output:

```
PS C:\Users\nadia\iot\demo> cp file file1
PS C:\Users\nadia\iot\demo>
```

---

### 15

Command: `mv file file2`

Expected Output: The mv command moves a file from one location to another. In this case it will move 'file' to 'file2'

Output:
```
PS C:\Users\nadia\iot\demo> mv file file2
PS C:\Users\nadia\iot\demo>
```

---

###16

Command: `rm file2`

Expected Output: The rm command will remove a file. In this case it will remove 'file2

Output: 
```
PS C:\Users\nadia\iot\demo> rm file2
PS C:\Users\nadia\iot\demo>
```

---

### 17

Command: `clear`

Expected Output: Will clear the terminal screen

Output: 

---

### 18

Command: `man uname`
