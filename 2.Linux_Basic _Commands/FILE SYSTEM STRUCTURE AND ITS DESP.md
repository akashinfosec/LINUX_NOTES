
Here are **short, exam-friendly notes** for each Linux file system directory:

| **Directory** | **Short Explanation**                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| **/** (Root)  | The top-most directory of the Linux file system. All other directories are inside it.                      |
| **/bin**      | Contains essential user commands like `ls`, `cp`, `mv`, `cat`, etc.                                        |
| **/boot**     | Stores bootloader files, Linux kernel, and files needed to start the operating system.                     |
| **/dev**      | Contains device files representing hardware such as hard disks, USB drives, keyboard, and terminals.       |
| **/etc**      | Stores system configuration files, startup scripts, and application settings.                              |
| **/home**     | Contains personal directories and files of all normal users.                                               |
| **/lib**      | Stores shared libraries and essential files required by programs in `/bin` and `/sbin`.                    |
| **/media**    | Mount point for removable devices like USB drives, CDs, and DVDs.                                          |
| **/mnt**      | Temporary mount point used to manually mount file systems or partitions.                                   |
| **/opt**      | Contains optional or third-party software packages installed by users.                                     |
| **/proc**     | A virtual file system that provides information about running processes and the Linux kernel.              |
| **/root**     | Home directory of the **root (superuser)** account.                                                        |
| **/run**      | Stores temporary runtime data such as process IDs (PIDs), sockets, and lock files.                         |
| **/sbin**     | Contains essential system administration commands used by the root user (e.g., `fdisk`, `mount`).          |
| **/srv**      | Stores data for services provided by the system, such as web servers or FTP servers.                       |
| **/sys**      | Virtual file system that provides information about hardware devices and the Linux kernel.                 |
| **/tmp**      | Stores temporary files created by applications. Usually cleared after reboot.                              |
| **/usr**      | Contains user applications, libraries, manuals, and documentation. Most installed software is stored here. |
| **/var**      | Stores variable data such as log files, cache files, spool files, and databases that change frequently.    |

### Easy way to remember

- **/** → Root of everything
    
- **/bin** → Basic commands
    
- **/boot** → Boot files
    
- **/dev** → Devices
    
- **/etc** → Configuration files
    
- **/home** → User files
    
- **/lib** → Libraries
    
- **/media** → USB/CD mounts
    
- **/mnt** → Temporary mounts
    
- **/opt** → Optional software
    
- **/proc** → Process information
    
- **/root** → Root user's home
    
- **/run** → Runtime data
    
- **/sbin** → System administration commands
    
- **/srv** → Service data
    
- **/sys** → System/Kernel information
    
- **/tmp** → Temporary files
    
- **/usr** → User programs
    
- **/var** → Variable data (logs, cache)