
## 📂 Navigating to the Project Directory

Navigate to the project directory:

```bash
cd /home/labex/project
```

Verify location:

```bash
pwd
```

List contents:

```bash
ls
```

## 🗑️ Removing a Single File

Check if `old_report.txt` exists:

```bash
ls old_report.txt
```

Remove it:

```bash
rm old_report.txt
```

Verify removal:

```bash
ls old_report.txt
```

⚠️ **No undo option! Be careful.**

## 🗑️ Removing Multiple Files

List `.tmp` files:

```bash
ls *.tmp
```

Remove them:

```bash
rm file1.tmp file2.tmp file3.tmp
```

Verify removal:

```bash
ls *.tmp
```

Use `-v` to see deleted files:

```bash
rm -v file1.tmp file2.tmp file3.tmp
```

## 📂 Removing a Directory

Check contents of `old_projects`:

```bash
ls old_projects
```

Try removing:

```bash
rm old_projects
```

(❌ Error: "Is a directory")

✅ Correct method:

```bash
rm -r old_projects
```

Verify removal:

```bash
ls old_projects
```

⚠️ **Be extra careful with `rm -r`!**

## 🛡️ Using `-i` for Safe Removal

Check file:

```bash
ls important_file.txt
```

Remove with confirmation:

```bash
rm -i important_file.txt
```

Confirm with `y` or cancel with `n`. Verify removal:

```bash
ls important_file.txt
```

## 🔥 Summary of `rm` Commands

|Command|Description|
|---|---|
|`rm filename`|Remove a single file|
|`rm file1 file2`|Remove multiple files|
|`rm -r directory`|Remove a directory and contents|
|`rm -i filename`|Interactive removal (asks for confirmation)|
|`rm -f filename`|Force removal without confirmation|
|`rm -v filename`|Verbose mode (shows deleted files)|

🚨 **Always double-check before using `rm`, especially with `-r` or `-f`!** 🚨

## Note: Difference between #rm and #rmdir

| Feature                       | `rm`                           | `rmdir`                                           |
| ----------------------------- | ------------------------------ | ------------------------------------------------- |
| Removes files                 | ✅ Yes                          | ❌ No                                              |
| Removes empty directories     | ✅ Yes                          | ✅ Yes                                             |
| Removes non-empty directories | ✅ Yes (with `-r`)              | ❌ No                                              |
| Requires confirmation         | ❌ No (unless `-i` is used)     | ✅ No error, just fails if non-empty               |
| Dangerous for system files    | 🚨 Yes (especially with `-rf`) | ⚠️ No (safe as it only removes empty directories) |