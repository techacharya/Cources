# File Hierarchy Structure in Linux System

Filesystem Hierarchy Standard describes directory structure, which defines the names, locations, and permissions for many file types and directories and its content in Unix and linux based Operating System.

### Purpose
  - Software to predict the location of installed files and directories, and
  - Users to predict the location of installed files and directories.

It is possible to define two independent distinctions among files: **` shareable `** v/s. **` unshareable `** and **` variable `** v/s. **` static `**. In general, files that differ in either of these respects should be located in different directories. This makes it easy to store files with different usage characteristics on different filesystems.
  - **Shareable** files are those that can be stored on one host and used on others. 
  - **Unshareable** files are those that are not shareable.
  - **Static** files include **` binaries `**, **` libraries `**, **` documentation files `** and other files that do not change without system administrator intervention. 
  - **Variable** files are files that are not static.

  ![static variable files](../../images/core-concept/linux-fhs/static-nonstatic.png)
  
Now we will discuss in detail about directories created by the linux system at the time of installation.
![directories at installation](../../images/core-concept/linux-fhs/linux-fhs.png)


### The root filesystem (/)
The contents of the root filesystem **` / `** must be adequate to boot, restore, recover, and/or repair the system.
  - To boot a system, enough must be present on the root partition to mount other filesystems. This includes **` utilities `**, **` configuration `**, **` boot loader `** information, and other essential start-up data.
  - To enable **` recovery `** and/or **` repair `** of a system, those utilities needed by an experienced administrator to diagnose and reconstruct a damaged system must be present on the root filesystem.
  - To restore a system, those utilities needed to restore from system backups must be present on the root filesystem.

The following directories, or symbolic links to directories, are required in **` / `**.
| **Directory** | **Description**                                   |
|---------------|---------------------------------------------------|
| **` bin `**   | Essential command binaries                        |
| **` boot `**  | Static files of the boot loader                   |
| **` dev `**   | Device files                                      |
| **` etc `**   | Host-specific system configuration                |
| **` lib `**   | Essential shared libraries and kernel modules     |
| **` media `** | Mount point for removeable media                  |
| **` mnt `**   | Mount point for mounting a filesystem temporarily |
| **` opt `**   | Add-on application software packages              |
| **` sbin `**  | Essential system binaries                         |
| **` srv `**   | Data for services provided by this system         |
| **` tmp `**   | Temporary files                                   |

usr Secondary hierarchy
var Variable data

