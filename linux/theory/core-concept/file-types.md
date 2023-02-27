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


