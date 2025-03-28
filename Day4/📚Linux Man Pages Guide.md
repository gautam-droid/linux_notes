## Man Overview

- **Man** is the built-in help system in Linux.
- **Man** is short for manual.
- A **man page** is documentation.
---

## Man Basics

- Read the **man** man page:
    
    ```bash
    man man
    ```
    
- Type **h** for help.
- Type **q** to quit.

---

## Man Page Navigation

**Man uses the less pager and Vim keybindings:**

| Key          | Action                  |
| ------------ | ----------------------- |
| **j**        | Forward (down) one line |
| **k**        | Backward (up) one line  |
| **Ctrl + f** | Forward one window      |
| **Ctrl + b** | Backward one window     |
| **g**        | Go to first line        |
| **G**        | Go to the last line     |

---

## Man Page Conventions

| Convention            | Meaning                               |
| --------------------- | ------------------------------------- |
| **bold text**         | Type exactly as shown.                |
| <u>_italic text_</u>  | Replace with an appropriate argument. |
| `[-abc]`              | Arguments within `[]` are optional.   |
| <code>-a \| -b</code> | Options cannot be used together.      |
| `argument ...`        | Argument is repeatable.               |

---

## Combining Options

- Only one hyphen (dash) is needed for multiple single-character options.

```bash
ls -l -h
ls -lh
```

- The same option can come in two forms:
    
    ```bash
    -w, --width=COLS
    ```
    
    Examples:
    
    ```bash
    ls --width=60
    ls -w 60
    ls -w60
    ```
    

---

## Man Page Sections

- Some commands may have **man pages** in different sections.
- You can specify the section to use:
    
    ```bash
    man SECTION_NUMBER PAGE
    ```
    
    Example:
    
    ```bash
    man 2 unlink
    ```
    

---

## Searching Man Pages

- Format:
    
    ```bash
    man -k regexp ...
    ```
    
- Example:
    
    ```bash
    man -k unlink
    ```
    
    Output:
    
    ```
    unlink (1) - call the unlink function
    unlink (2) - delete a name
    ```
    

---

## Getting Help from Commands

- Common options for additional help:
    
    ```bash
    --help
    -h
    ls --help
    ```
    

---

## Getting Help with Shell Builtins

- Format:
    
    ```bash
    help [pattern ...]
    ```
    
    Example:
    
    ```bash
    help while
    ```
    
- Format:
    
    ```bash
    type name [name ...]
    ```
    
    Example:
    
    ```bash
    type ls
    ```

#note:
- **`help`** is a shell feature and works only for built-in commands.
- **`--help`** is an option that external commands implement to provide quick usage information.
- If a command doesn't support `--help`, try `man command` instead!