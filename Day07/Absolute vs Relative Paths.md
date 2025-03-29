## **1. Absolute Path**

- Always starts from the **root directory (`/`)**.
- Works **independently** of the current working directory (`pwd`).
- Example:
    
    ```bash
    ls /home/gautam/new/newapp/config.txt
    cd /var/log
    cat /etc/passwd
    ```
    
- If a path **starts with `/`**, it is **absolute**.
- **You cannot type an absolute path without the `/` at the beginning.**

---

## **2. Relative Path**

- Depends on the **current directory (`pwd`)**.
- Does **not** start with `/`.
- Examples:
    
    ```bash
    ls new/newapp/config.txt  # Relative to current directory
    cd ../  # Move one level up
    ```
    
- `.` (dot) → Current directory.
- `..` (double dot) → Parent directory.
- Example:
    
    ```bash
    ls ./config.txt   # Same as ls config.txt
    ls ../docs/       # Lists contents of the parent directory
    ```
    

---

## **3. Dummy Directory Structure for Examples**

Consider the following directory structure:

```
/home/gautam/
├── new/
│   ├── newapp/
│   │   ├── config.txt
│   ├── docs/
│   │   ├── readme.md
│   ├── backup/
```

All examples will refer to paths based on this structure.

---

## **4. Special Case: `~` (Home Directory)**

- `~` is **not technically absolute** but behaves like an absolute path.
- Expands to **`/home/username/`**.
- Works for any user:
    
    ```bash
    echo ~  # Expands to /home/gautam/
    ls ~/new/config.txt  # Same as ls /home/gautam/new/config.txt
    ```
    
- `~username/` can be used to access another user's home directory:
    
    ```bash
    ls ~otheruser/
    ```
    

---

## **5. Differences Between Absolute & Relative Paths**

|Feature|Absolute Path|Relative Path|
|---|---|---|
|Starts With|`/`|No `/`|
|Works From Any Location|✅ Yes|❌ No|
|Depends on `pwd`|❌ No|✅ Yes|
|Example|`/home/gautam/file.txt`|`newapp/file.txt`|
|Moves Up Directory?|❌ No|✅ `..`|
|Uses `~`?|✅ Expands to absolute|❌ No|

---

## **6. Common Mistakes & Fixes**

### **A. Using a Relative Path Instead of an Absolute One**

❌ **Wrong:**

```bash
ls home/gautam/file.txt  # No leading /
```

✅ **Correct:**

```bash
ls /home/gautam/file.txt
```

### **B. Forgetting `..` for Parent Directory**

❌ **Wrong:**

```bash
ls newapp/config.txt  # Works only if `newapp/` is in current directory
```

✅ **Correct:**

```bash
ls ../newapp/config.txt  # Moves up one directory first
```

**Where You Are (`pwd` before the command):**

```
/home/gautam/new/docs/
```

**What Happens When You Run `ls ../newapp/config.txt`?**

- `..` moves **one level up** to `/home/gautam/new/`.
- `newapp/config.txt` is then accessed from `/home/gautam/new/newapp/config.txt`.

### **C. Using `~` Incorrectly**

❌ **Wrong:**

```bash
ls ~/docs/readme.md  # Fails if `~/docs/` does not exist
```

✅ **Correct:**

```bash
ls ~/new/docs/readme.md
```

---

## **7. Advanced Path Navigation Tricks**

### **A. Returning to the Previous Directory**

```bash
cd -  # Switches back to the last directory
```

### **B. Finding Files Using Relative Paths**

```bash
find . -name "config.txt"  # Searches for config.txt from current directory
```

### **C. Copying Files Using Relative Paths**

```bash
cp newapp/config.txt ../backup/
```

- Copies `config.txt` from `newapp/` to `backup/` (one level up).

---

## **8. Final Summary**

- **Absolute paths** start with `/` and work from anywhere.
- **Relative paths** depend on `pwd` and do **not** start with `/`.
- **`~` is a shortcut for the home directory** but **not a true absolute path**.
- Use `.` (current directory) and `..` (parent directory) for navigation.
- **You cannot type an absolute path without the `/` at the beginning.**
- If in doubt, check your path with:
    
    ```bash
    pwd  # Print current working directory
    ```
    

🚀 **Master these, and you'll never get lost in the file system again!**