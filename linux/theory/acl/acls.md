# Access Control Lists (ACLs) in linux
The files and directories have permission sets (a combination of read, write and execute permissions) for the owner of the file, the group associated with the file, and all other users for the system. However, these permission sets have some limitations. For example, different permissions cannot be configured for different users. Access control lists **_(ACLs)_** provide a finer-grained access control mechanism than these traditional Linux access permissions. There are two types of **_ACLs_**:
  - **_access ACLs_**
  - **_default ACLs_**

#### access ACLs
An access **_ACL_** is the access control list for a specific file or directory. 

#### default ACLs
A default ACL can only be associated with a directory and the **_default ACLs_** are optional.

**_ACLs can be configured:_** <br>
  - _Per user_
  - _Per group_
  - _Via the effective rights mask_
  - _For users not in the user group for the file_

The **` setfacl `** and **` getfacl `** utilities are used for setting up **_ACLs_** and retrieving **_ACLs_** respectively.

### Retrieving ALCs
To determine the existing **_ACLs_** for a file or directory, _**` getfacl `**_ commandis is used. When a file does not have an **_ACL_**, it displays the same information as _**` ls –l `**_, although in a different format. To retrieve the access control lists for a file or directory execute the following command:
```
$ getfacl /home/acharya/course/welcome.sh
```
![Retrieving ACLs](../../images/acls/retrieve-acl.png)

Here, **_welcome.sh_** file and directory **_tech_acharya_** directory does not have the **_ACL_**.



