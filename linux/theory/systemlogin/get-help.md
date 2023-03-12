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
| **Selection-num** | **Description**                                                                |
|--------------------|--------------------------------------------------------------------------------|
| **1**              | Executable programs or shell commands                                          |
| **2**              | System calls (functions provided by the kernel)                                |
| **3**              | Library calls (functions within program libraries)                             |
| **4**              | Special files (usually found in /dev)                                          |
| **5**              | File formats and conventions, e.g. /etc/passwd                                 |
| **6**              | Games                                                                          |
| **7**              | Miscellaneous (including macro packages and conventions), e.g. man(7), groff(7)|
| **8**              | System administration commands (usually only for root)                         |
| **9**              | Kernel routines [Non standard]                                                 |

### Update manual database cache using mandb
**` mandb `**  is  used to initialise or manually update index database caches.  The caches contain information relevant to the current state of the manual page system and the information stored within them is used by the **_man-db_** utilities to enhance their speed and functionality.

Supplying **` mandb `** with an optional colon-delimited path will override the internal system manual page hierarchy search path, determined from information found within the **_man-db_** configuration file.

If manual of any command not found in that case execute the **` mandb `** command to update database cache.
```
$ mandb
```
### The which command
**` which `** command takes one or more arguments. For each of its arguments it prints to **_stdout_** the full path of the executables that would have been executed when this argument had been entered at the shell prompt. It does this by searching for an executable or script in the directories listed in the environment variable **_PATH_**.
**_Syntax:_** <br>
```
$ which command/keywords
```
**_Example:_**
```
$ which ls
```

### Tab Completion
Tab completion can save you keystrokes, prevent spelling mistakes, and guide you through complex commands. It works with file names, commands, command arguments, and more.

All of the modern shells have command and filename completion via the **` Tab `** key. The basic principle in all of these shells is the same; you type the start character of the keyword or command, hit the **_Tab_** key twice, and the list of possible commands or files is displayed. 
```
$ mk <Tab> <Tab>
```
**OR**
```
$ ls -ltrh /etc/ssh/ <tab><tab>
```

### Additional information
To explore more in depth read the below manuals:
```
$ man bash
$ man intro
$ man man
$ man help
```




