# File Permissions in linux Systems

Linux is the **_multi-user_** operating system which can be accessed by many users simultaneously. But this raises security concerns as an unsolicited or malign user can corrupt, change or remove crucial data. For effective security, linux divides authorization into two levels.
  1. **_Ownership_**
  2. **_Permission_**

     ![Ownership & permission](../../images/file-permission/file-permission.png)

#### File and Directory Ownership
Each and every file/directory is owned by a specific user or UID and a specific group or GID. Every file and directory on Unix/Linux system is assigned 3 types of owner, listed below.
  - **_User:_** <br>
    A user is the one who created the file. By default, whosoever, creates the file becomes the owner of the file. User can create, delete, or modify the file.
  - **_Group:_** <br>
     A group can contain multiple users. All the users belonging to a group have same access permission for file or directory.
  - **_Other:_** <br>
    Any one who has access to the file or directory other than user and group comes in the category of other. Other has neither created the file nor is a group member.

 

