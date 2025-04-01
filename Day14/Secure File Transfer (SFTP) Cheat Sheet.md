## 🔗 Connecting to SFTP Server  
```bash
sftp username@ip
sftp -v username@ip  # Enable verbose mode
````

---

## 📂 Directory Navigation

|Command|Description|
|---|---|
|`pwd`|🔍 Show **current remote directory**|
|`lpwd`|🖥️ Show **current local directory**|
|`cd /path`|📂 Change **remote directory**|
|`lcd /path`|🏠 Change **local directory**|

---

## 📜 Listing Files

|Command|Description|
|---|---|
|`ls`|📋 List **remote** files|
|`lls`|🗂️ List **local** files|

---

## 📤 Uploading Files

|Command|Description|
|---|---|
|`put filename`|⬆️ Upload a **single file**|
|`mput *.txt`|📂 Upload **multiple files**|

---

## 📥 Downloading Files

|Command|Description|
|---|---|
|`get filename`|⬇️ Download a **single file**|
|`mget *.txt`|📥 Download **multiple files**|

---

## 📁 Directory Management

|Command|Description|
|---|---|
|`mkdir remoteDir`|🏗️ Create a **directory on remote** machine|
|`lmkdir localDir`|🏠 Create a **directory on local** machine|

---

## 🗑️ Deleting Files & Directories

|Command|Description|
|---|---|
|`rm filename`|❌ Remove a **file** on remote machine|
|`rmdir foldername`|🗑️ Remove a **directory** on remote machine|

---

## 🚪 Exiting SFTP

```bash
exit
```

🔚 **Close the SFTP session safely**

---
