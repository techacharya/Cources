# File types in Linux based system

In Linux based system each and everything is considered as file. Even **` hard disk `**, **` printer `**, **` Network Interface Card `**, etc. is a file in linux based Operating system.

There are mainly three types of files available in linux system.
  - Regular Files
  - Directory files
  - Special Files

  ![file types](../../images/core-concept/file-types/file-type.png)

### Regular Files
Regular Files are general ordinary files in the system  that contains **` programs `**, **` scripts `**, **` texts `**, **` images `**, **` data `** and so on. To check this execute the command:
```
$ ls -ltr | grep ^-
```


### Directory Files
Directory files are those files taht contains the other files and directory and their related information (meta data). To view this execute the below command either **` find / -type d `** or **` ls -ltr | grep ^d `**.
```
$ ls -l | grep ^d
```

### Special Files
Special files are further categorised into different types listed below:
  - Block Files
  - Character Files
  - Socket Files
  - Symbol Link Files
    - Soft Link
    - Hard Link
  - Named Pipe files

  ![Special Files Types](../../images/core-concept/file-types/special-file-type.png)
  

### Block Files
Block files act as a direct interface to block devices that performs data **Input** and **Output** operations in units of blocks. These files are hardware files and most of them are present in **` /dev `**. 
