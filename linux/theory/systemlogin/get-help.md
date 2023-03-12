# Getting help in linux System

Whenever we use the new environment, sometimes it is complex to us and we are completely clueless. In this situation, we need someone to guide us or some kind of help from the new environment to deal with. 

In linux systems thausands and thausand commands and files are avaialbe to perform various activity and to remember all these commands, purpose and location of that files and commands are difficult for human being. Even if we remember the command name, but due to not using it frequently, we forget the usage of the command many times. So need some kind of help to deal with all this.


To full fill all these purpose, almost every software and operating system has some kind of built-in help to assist naive and inexperienced users. So we can get help from environment itself to do the basic lebel of troubleshoot or for better understanding of command usage.


### The command option **_-h_** or **_--help_**
To know the usage of command and how to use the options with the command and what are they and their purpose make use of **` -h `** or **` --help `** option with command.
**_Syntax:_** <br>
```
$ command -h          OR       $ command --help
```
**_Example:_** <br>
```
$ ls --help
```


### The man command
The **` man `** command is short for manual, it displays the detail information about command or tool or utility that we can run on
the terminal. A user can request to display a manual page by simply typing **` man `** followed by a space and then **` argument `** argument can be a command, utility or function. <br>

**_Syntax:_** <br>
```
$ man [OPTION]... [COMMAND NAME]...
```
**_Example:_** <br>
```
$ man -k fdisk
```
  - If **_OPTION_** is not used, it displays the whole manual of the command. <br>
    **_Syntax:_** <br>
    ```
    $ man [COMMAND NAME]
    ```
    **_Example:_** <br>
    ```
    $ man passwd
    ```
  - **Section-num:** Since a manual is divided into multiple sections so this option is used to display
only a specific section of a manual. <br>
    **_Syntax:_** <br>
    ```
    $ man [SECTION-NUM] [COMMAND NAME]
    ```
    **_Example:_** <br>
    ```
    $ man 8 fdisk
    ```

Every manual is divided into the following sections:
| ** Selection-num** | **Description**                                                                |
|--------------------|--------------------------------------------------------------------------------|
| **1**              | Executable programs or shell commands                                          |
| **2**              | System calls (functions provided by the kernel)                                |
| **3**              | Library calls (functions within program libraries)                             |
| **4**              | Special files (usually found in /dev)                                          |
| **5**              | File formats and conventions, e.g. /etc/passwd                                 |
| **6**              | Games                                                                          |
| **7**              | Miscellaneous (including macro packages and conventions), e.g. man(7), grff(7) |
| **8**              | System administration commands (usually only for root)                         |
| **9**              | Kernel routines [Non standard]                                                 |



