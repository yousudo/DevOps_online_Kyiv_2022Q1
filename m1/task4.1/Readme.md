<a id="anchor"></a>

# Linux Essentials

## Task 4.1 Part 1

---

### _Using the passwd Command_

+ The passwd command modifies such files
  - /etc/passwd - contains information about users
  - /etc/shadow - contains information about system user passwords
  - /etc/pam.d/passwd — PAM settings for passwd (Authentication Modules)

![Passwd](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/passwd.png "Passwd")

### _System Users_

![user](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/users.png "user")


![allusers](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/all_users.png "allusers")


![shadow_file](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/passwd_shadow_file.png "shadow_file")

+ From the following screenshot, we can find out such information
1. Username
2. The encrypted password ( x represents the stored 3.password)
4. User identification number (UID)
5. User group identification number (GID)
6. Full name, phone number , e-mail etc.
7. User home directory
8. User login shell (default is bash shell)

![passwd_file](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/passwd_file.png "passwd_file")

### _Changing user information_

![chfn](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/chfn.png "chfn")

### _Man and info commands._

`man passwd`
`info passwd` 
`passwd -l, --lock `
           Lock the password of the named account.
`passwd -u, --unlock`
           Unlock the password of the named account.      


### _View the contents of files .bash* using commands_

![.bash*](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/cat.png ".bash*")

### _User plan_

` nano ~/.plan `

![User plan](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/finger.png "User plan")

### _ls command_

![ls](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/ls.png "ls")

---

## Task 4.1 Part 2

### _Tree command_

`tree -ifa Documents` 
`tree -a /etc`
`tree -P "*c*"`

![tree](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/tree1.2.png "tree")

### _File command_

`file NAME`
`file *`

![file](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/file1.2.png "file")

### _Navigating the file system_

`cd`
`cd ~/dir`
`cd /home/dir`

### _Ls command_

+ key "l" - displays owner, group, creation date, size, etc
+ key "a" - displays all files, even hidden ones.

![ls](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/ls1.2.png "ls")

### _Ls command_

`mkdir dir` 
`ls -a > dir/home_dir.txt`
`cat dir/home_dir.txt`
`cp dir/home_dir.txt ~/`
`rm -rfi dir`
`rm home_dir.txt`

### _links in Ubuntu_

+ In the case of a symbolic link, we simply refer to a directory or file (for example, to access this file from the desktop - an analogue of a shortcut in Windows), when the file is deleted, the link will become inactive.
Hard link (duplicate file) - created only on the file, when the parent file is deleted, the hard link will remain available and save all the changes that were made in the file.

+ When changing data with a symbolic link, the source file will change.

+ Changing the hard link file changes both files.
`mkdir test`
`cp .bash_history test/labwork2`
`cd test`
`ln -s /home/re/test/labwork2 labwork2.link`
`ln /home/re/test/labwork2 labwork2.dublicate`

![link](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/link1.2.png "link")

+ After deleting the original file, when following a symbolic link, the data will not be available, since we referred to the labwork2 file.

+ After deleting the original file, the data will remain available when following a hard link, because we actually made a duplicate of the labwork2 file
`mv labwork2.dublicate hard_lnk_labwork2`
`mv labwork2.link symb_lnk_labwork2`
`rm labwork2`

![link2](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/link2_1.2.png "link2")

### _locate utility_

`locate squid`
`locate traceroute`

### _Mounted partitions_

`sudo blkid`

![dev_mount](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/dev_mount1.2.png "dev_mount")

### _Count the number in "locate"_

`locate -c traceroute`

![locate](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/locate%20-c1.2.png "locate")

### _Find command"_

`sudo find /etc -name "*host*"`
`sudo find /etc -name "*ss*"`
`ls -la /etc | grep ss`

### _Redirection operations_

`ls -la /etc > etc.txt`

### _Types of devices_

There are such types of devices in Linux

+ Symbol device - cd drive, etc. (Byte-oriented) devices read and write data as a stream of bytes.

+ Block device - hard disk, ssd disk, etc. Block-oriented devices read and write data in blocks.
The device type can be determined by the first letter in the permission list (`ls -l`), b is a block, c is a character.

### _Types of file_

There are such file types in Linux

+ Regular files
  + Text files
  + Executable files
  + Image files
  + Archive files
  + Program Library Files

+ Special Files
  + Block
  + Symbolic.
  + Symbolic links
  + Tunnels/named tunnels
  + Tunnels/named tunnels
  + Socket files

+ Catalogs

The file type can be determined with the command `file *` `file NAME`

![file](https://github.com/yousudo/DevOps_online_Kyiv_2022Q1/blob/develop/m1/task4.1/file1.2.png "file" )

### _Item 15_

`sudo find /etc -type f -printf '%TY-%Tm-%Td %TT %p\n' | sort | tail -n5`


[UP](#anchor)
