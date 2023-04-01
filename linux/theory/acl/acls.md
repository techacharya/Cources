# Access Control Lists (ACLs) in linux
The files and directories have permission sets (a combination of read, write and execute permissions) for the owner of the file, the group associated with the file, and all other users for the system. However, these permission sets have some limitations. For example, different permissions cannot be configured for different users. Access control lists **_(ACLs)_** provide a finer-grained access control mechanism than these traditional Linux access permissions. There are two types of ACLs:
  - **_access ACLs_**
  - **_default ACLs_**

#### access ACLs
An access **_ACL_** is the access control list for a specific file or directory. 

#### default ACLs
A default ACL can only be associated with a directory and the **_default ACLs_** are optional.
