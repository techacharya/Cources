# File Permissions in linux Systems

Linux is the **_multi-user_** operating system which can be accessed by many users simultaneously. But this raises security concerns as an unsolicited or malign user can corrupt, change or remove crucial data. For effective security, linux divides authorization into two levels.
  1. **_Ownership_**
  2. **_Permission_**

     ![Ownership & permission](../../images/file-permission/file-permission.png)

### File and Directory Ownership
Each and every file/directory is owned by a specific user or UID and a specific group or GID. Every file and directory on Unix/Linux system is assigned 3 types of owner, listed below.
  - **_User:_** <br>
    A user is the one who created the file. By default, whosoever, creates the file becomes the owner of the file. User can create, delete, or modify the file.
  - **_Group:_** <br>
     A group can contain multiple users. All the users belonging to a group have same access permission for file or directory.
  - **_Other:_** <br>
    Any one who has access to the file or directory other than user and group comes in the category of other. Other has neither created the file nor is a group member.
    ![file owners](../../images/file-permission/file-owners.png)

 
### File and Directory Permission
File permissions are core to the security model used by linux systems. They determine who can access files and directories on a system and how. This article provides an overview of linux file permissions, how they work, and how to change them.

#### View File and Directory Permission
To view file or directory permission execute the **` ls `** command along with its **` -l `** (for long listing) option will show you metadata about linux files, including the permissions set on the file and directory.
```
$ ls -l
```
![Ownership & permission](../../images/file-permission/view-permission.png)

In above example, you see three different content entry. The first field of the **` ls -l `** output is a group of metadata that includes the permissions on each file. Here are the components of the **_hello.py_** listing:
  - File type: **_-_**
  - Permission settings: **_rw-rw-r--_**
  - Extended attributes: **_._**
  - Number of hard links: **_1_**
  - User owner: **_acharya_**
  - Group owner: **_acharya_**
  - Size in block: **_0_**
  - Last modified or created date and time: **_Mar 30 15:45_**
  - File or directory name itself: **_hello.py_**

#### Read file and Directory Permission
The **_permission settings_** on a file or directory has the set of permissions for owners (user, group and others) to **` read `**, **` write `** and **` execute `**. The interesting permissions from the **_hello.py_** listing are as follow:


