## Changing File Ownership

- **Check Current Ownership:**
  ```sh
  ls -l example.txt
  ```
  Output:
  ```sh
  -rw-rw-r-- 1 labex labex 0 Jul 29 15:11 example.txt
  ```
  - This command lists the file details, showing permissions, owner, group, symbolic links, size, and modification date.

- **Change Ownership to `root`:**
  ```sh
  sudo chown root:root example.txt
  ```
  - `sudo` is used to run the command with root privileges.
  - `chown` changes the ownership of the file to the specified user and group.

- **Verify Change:**
  ```sh
  ls -l example.txt
  ```
  Output:
  ```sh
  -rw-rw-r-- 1 root root 0 Jul 29 15:11 example.txt
  ```
  - This confirms the ownership has been changed to `root`.

## Changing Directory Ownership

- **Create Directory and Files:**
  ```sh
  mkdir -p new-dir/subdir
  echo "Hello, world" > new-dir/file1.txt
  echo "Another file" > new-dir/subdir/file2.txt
  ```
  - Creates a directory structure and files within it.

- **Check Current Ownership:**
  ```sh
  ls -lR new-dir
  ```
  - Lists the directory contents recursively, showing ownership details.

- **Change Ownership Recursively:**
  ```sh
  sudo chown -R root:root new-dir
  ```
  - `-R` option changes ownership for the directory and all its contents.

- **Verify Change:**
  ```sh
  ls -lR new-dir
  ```
  - Confirms the ownership change for the directory and its contents.

## Changing File Permissions

- **Check Current Permissions:**
  ```sh
  ls -l example.txt
  ```
  - Lists the file details, showing current permissions.

- **Change Permissions:**
  ```sh
  sudo chmod 700 example.txt
  ```
  - `chmod` changes the file permissions to `700` (read, write, execute for owner only).

- **Verify Change:**
  ```sh
  ls -l example.txt
  ```
  Output:
  ```sh
  -rwx------ 1 root root 0 Jul 29 15:11 example.txt
  ```
  - Confirms the permission change.

# Linux Directory Permissions

- **Read permission (r)** allows you to list the contents of the directory using `ls`.  
- **Write permission (w)** allows you to create new files and subdirectories within the directory.  
- **Execute permission (x)** allows you to access files and sub directories within the directory (i.e., `cd` into it).  

## Changing Directory Permissions

- **Create Directory:**
  ```sh
  mkdir ~/test-dir
  ```
  - Creates a new directory.

- **Change Permissions:**
  ```sh
  chmod 700 ~/test-dir
  ```
  - Changes the directory permissions to `700` (read, write, execute for owner only).

- **Verify Change:**
  ```sh
  ls -ld ~/test-dir
  ```
  - The `-d` option in `ls -l` tells `ls` to list the directory itself, rather than its contents. Without `-d`, `ls` would list the files and sub directories _inside_ `test-dir`

- **Change Permissions Recursively:**
  ```sh
  chmod -R 755 ~/test-dir
  ```
  - `-R` option changes permissions for the directory and all its contents to `755` (read, write, execute for owner; read, execute for group and others).

- **Verify Change:**
  ```sh
  ls -ld ~/test-dir
  ```
  - Confirms the permission change for the directory and its contents.

## Using Symbolic Notation for Permissions

## Basic Symbols
- **User Types**:
  - `u` → User (owner)
  - `g` → Group
  - `o` → Others
  - `a` → All (u, g, o)

- **Permission Types**:
  - `r` → Read
  - `w` → Write
  - `x` → Execute

- **Operators**:
  - `+` → Add permission
  - `-` → Remove permission
  - `=` → Set exact permission (override)


- **Create Script:**
  ```sh
  cd ~/project
  echo '#!/bin/bash\necho "Hello, World"' > script.sh
  ls -l script.sh
  ```
  - Creates a new script file and lists its details.

- **Run Script (Permission Denied):**
  ```sh
  ./script.sh
  ```
  - Attempts to run the script, but fails due to lack of execute permission.

- **Add Execute Permission:**
  ```sh
  chmod u+x script.sh
  ls -l script.sh
  ```
  - `u+x` adds execute permission for the owner.

- **Run Script Again:**
  ```sh
  ./script.sh
  ```
  Output:
  ```sh
  Hello, World
  ```
  - Successfully runs the script after adding execute permission.

## Detailed Examples

| Command                                                  | Description                                                                |
| -------------------------------------------------------- | -------------------------------------------------------------------------- |
| `chmod u+x file`                                         | Add execute permission for user                                            |
| `chmod g-w file`                                         | Remove write permission for group                                          |
| `chmod o+r file`                                         | Add read permission for others                                             |
| `chmod a-x file`                                         | Remove execute permission for all                                          |
| `chmod u=rwx,g=rx,o=r file`                              | Set exact permissions                                                      |
| `chmod ug+rw,o+x file`                                   | Add read & write for user and group, execute for others                    |
| `chmod u-wx,g-r,o-rx file`                               | Remove write & execute for user, read for group, read & execute for others |
| `chmod a+rw file`                                        | Add read & write permissions to everyone (user, group, others)             |
| `chmod a-rwx file`                                       | Remove all permissions from everyone                                       |
| `chmod a-r-w+x file` or              `chmod a-rw+x file` | Remove read,write permission and add execute permission                    |

