## Creating a Backup of a File
To create a backup of `important_report.txt` in the same directory:

```bash
cp ~/project/important_report.txt ~/project/important_report_backup.txt
````

This command copies the `important_report.txt` to a new file `important_report_backup.txt`.

## Copying Files to Different Directories

To copy `favorite_song.mp3` to the `music` directory:

```bash
cp ~/project/favorite_song.mp3 ~/project/music/
```

## Copying Multiple Files at Once

To copy multiple text files to the `documents` directory:

```bash
cp ~/project/report1.txt ~/project/report2.txt ~/project/notes.txt ~/project/documents/
```

## Using the `-i` Option for Interactive Copying

To avoid accidental overwriting, use the `-i` option:

```bash
cp -i ~/project/new_test_file.txt ~/project/test_file.txt
```

It will prompt for confirmation before overwriting files.

## Recursive Copying with the `-r` Option

To copy an entire directory (`websiteRelatedStuff`) and its contents:

```bash
cp -r ~/project/websiteRelatedStuff ~/project/websiteRelatedStuff_backup
```

## Preserving File Attributes with the `-p` Option

To copy a file and preserve its attributes (timestamps, permissions):

```bash
cp -p ~/project/old_file.txt ~/project/preserved_file.txt
```

- The `-p` option stands for "preserve". It maintains the original file's modification time, access time, and permissions.
## Using Wildcards for Selective Copying

To copy all `.txt` files to the `text_files` directory:

```bash
cp ~/project/*.txt ~/project/text_files/
```

To copy all `.pdf` files to the `pdf_files` directory:

```bash
cp ~/project/*.pdf ~/project/pdf_files/
```

## Additional `cp` Options:

- `-u`: Copy only if the source file is newer or missing in the destination.
    
- `-v`: Verbose mode, explaining each action.
    
- `-n`: No overwrite (don’t overwrite existing files).
    
- `-l`: Create hard links instead of copying.
    
- `-s`: Create symbolic links instead of copying.
### Additional `cp` Options with commands:

#### `-u`: Copy only if the source file is newer or missing in the destination.
```bash
cp -u ~/project/source_file.txt ~/project/destination_file.txt
````

#### `-v`: Verbose mode, explaining each action.

```bash
cp -v ~/project/source_file.txt ~/project/destination_file.txt
```

#### `-n`: No overwrite (don’t overwrite existing files).

```bash
cp -n ~/project/source_file.txt ~/project/destination_file.txt
```

#### `-l`: Create hard links instead of copying.

```bash
cp -l ~/project/source_file.txt ~/project/hard_link_file.txt
```

#### `-s`: Create symbolic links instead of copying.

```bash
cp -s ~/project/source_file.txt ~/project/symbolic_link_file.txt
```

---

