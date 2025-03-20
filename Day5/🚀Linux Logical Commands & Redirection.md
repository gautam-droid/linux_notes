
## **Introduction**
This guide introduces essential Linux command-line tools: **logical operators**, **redirection**, and **pipelines**. These tools help control program execution, manage input/output, and improve efficiency in Linux environments.

---

## **Logical Operators**

### **Logical AND (&&)**
- Runs the second command **only if** the first command **succeeds**.
  ```sh
  mkdir test_dir && echo "Directory created successfully"
  ```
- If `mkdir test_dir` fails, the `echo` command **will not execute**.

### **Logical OR (||)**
- Runs the second command **only if** the first command **fails**.
  ```sh
  mkdir test_dir || echo "Failed to create directory"
  ```
- If `mkdir` succeeds, `echo` **is skipped**.

### **Command Separator (;)**
- Executes **all** commands **sequentially**, regardless of success/failure.
  ```sh
  echo "First command" ; echo "Second command" ; echo "Third command"
  ```
- Useful when commands are **independent** of each other.

---

## **Output Redirection**

### **Basic Redirection (>)**
- Redirects output to a file (overwrites existing content).
  ```sh
  echo "Hello, World" > greeting.txt
  cat greeting.txt
  ```

### **Appending Output (>>)**
- Appends output **without** overwriting the existing file.
  ```sh
  echo "First line" > multiline.txt
  echo "Second line" >> multiline.txt
  echo "Third line" >> multiline.txt
  cat multiline.txt
  ```

---

## **Pipelines (|)**
- **Pipes (|)** pass output from one command to another.
  ```sh
  echo "apple banana cherry" | tr ' ' '\n' | sort
  ```
- `tr` converts spaces to newlines, and `sort` orders the output.

### **Combining Logical Operators & Redirection**
```sh
echo "The quick brown fox jumps over the lazy dog" > sentence.txt
cat sentence.txt | grep "fox" > fox_result.txt && echo "Search completed successfully" || echo "Search failed"
cat fox_result.txt
```
- **Creates** `sentence.txt`.
- **Searches** for "fox" and **redirects** output to `fox_result.txt`.
- **Prints success message** if `grep` finds a match, otherwise prints failure message.

### **Why Does Grep Output the Full Line Instead of Just the Word?**
- `grep` by default prints the **entire matching line** when searching for a pattern.
- If you want **only the matched word**, use:
  ```sh
  grep -o "fox" sentence.txt
  ```
- The `-o` option extracts **only the matching text** instead of the full line.

---

## **Super User (Root User)**
- The **super user (root)** has **full control** over the system.
- Used for **system modifications, software installation, and user management**.
- Can be accessed using:
  ```sh
  # Switch to root (requires root password)
  su -
  
  # Run a command as root (requires user password, logs command usage)
  sudo <command>
  ```
- **`su`** switches the user to root.
- **`sudo`** runs a command as another user (default: root) **and logs commands**.
- **Warning:** Root privileges should be handled **carefully** to prevent system damage.

---

## **Conclusion**
- **Logical operators** (`&&`, `||`, `;`) help control command execution.
- **Redirection** (`>`, `>>`) manages output files.
- **Pipelines (`|`)** chain commands for advanced processing.
- **Super user privileges** allow administrative control but should be used cautiously.
- **Grep prints full lines by default**, use `-o` for only the matched word.

By mastering these concepts, you can efficiently navigate and manage Linux systems!
