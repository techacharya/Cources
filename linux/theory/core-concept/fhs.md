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
| **` etc `**   | Host specific system configuration                |
| **` lib `**   | Essential shared libraries and kernel modules     |
| **` media `** | Mount point for removeable media                  |
| **` mnt `**   | Mount point for mounting a filesystem temporarily |
| **` opt `**   | Add-on application software packages              |
| **` sbin `**  | Essential system binaries                         |
| **` srv `**   | Data for services provided by this system         |
| **` tmp `**   | Temporary files                                   |
| **` usr `**   | Secondary hierarchy                               |
| **` var `**   | Variable data                                     |
| **` home `**  | User's home directories (optional)                |
| **` root `**  | Home directory for the root user (optional)       |

### /bin
**` /bin `** contains commands that may be used by both the system administrator and by users. It may also contain commands which are used indirectly by scripts.

### /boot
This directory contains everything required for the **` boot process `** except configuration files not needed at boot time and the map installer. Thus /boot stores data that is used before the kernel begins executing user-mode programs. The kernel must be located in **` /boot `**.

### /dev
The **` /dev `** directory is the location of device files and/or special files.

### /etc
The **` /etc `** the name stands for **` editable text configuration `** contains configuration files. A **` configuration file `** is a local file used to control the operation of a program it must be static and cannot be an executable binary.

### /lib
The **` /lib `** directory contains those shared library images needed to boot the system and execute the commands in the root filesystem, i.e. by binaries in **` /bin `** and **` /sbin `**.

### /media
Default mount point for removable devices, such as USB sticks, media players, cdroms, etc.

### /mnt
This directory is provided so that the system administrator may temporarily mount a filesystem as needed. The content of this directory is a local and should not affect any program is run.

### /opt
The **` /opt `** directory is reserved for the installation of add-on application software packages. A package to be installed in **` /opt `** must locate its static files in a separate **` /opt/<package> `** or **` /opt/<provider> `** directory tree, where <package> is a name that describes the software package and <provider> is the provider’s LANANA (Linux Assigned Names And Numbers Authority) registered name.

### /sbin
Utilities used for **` system administration `** root-only commands are stored in **_ /sbin _**, **_ /usr/sbin _**, and *_ /usr/local/sbin _*. **` /sbin `** contains binaries essential for **_ booting _**, **_ restoring _**, **_ recovering _**, and/or **_repairing _** the system in addition to the binaries in **` /bin `**.
  

  


