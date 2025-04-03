
---

### **🔑 Setting Up SSH Key-Based Authentication**

#### **1️⃣ Start the SSH Server on the Host Machine**

🚀 Run the following command on your **host machine** to start the SSH server:

```bash
sudo systemctl start ssh
```

🔍 To check the status, run:

```bash
sudo systemctl status ssh
```

---

#### **2️⃣ Generate an SSH Key on the Client Machine**

✅ **Before proceeding, check if any key is present in the host machine's `.ssh` folder:**

```bash
cd ~/.ssh
ls
```

If there are any keys present, like `id_rsa`, `id_ed25519`, or any other name, choose a different file name unless you want to overwrite it.

💻 Now, on your **client** machine (yes, you heard it right), generate an SSH key pair by running:

```bash
sudo ssh-keygen -b 4096
```

> **ℹ️ Note:** The `-b` flag specifies the key length in bytes (4096 in this case).

✅ When prompted for the filename, **hit enter** to use the default location (`~/.ssh/id_rsa`) if no existing keys are present.  
⚠️ If a file already exists in `~/.ssh/`, it's recommended to specify a **custom filename** (don't forget to provide the full path, or it will be created in your current directory):

```bash
~/.ssh/customFileName
```

🎯 Press **enter** to continue.

---

#### **3️⃣ Copy the Public Key to the Host Machine**

💡 **Tip:** It doesn't matter where you generate the key. What matters is that the **private key** should remain on the client machine, and the **public key** should be on the host machine. If needed, you can also transfer it manually.

📤 To copy the **public key** to the host machine from the client machine, run:

```bash
ssh-copy-id -i ~/.ssh/customFileName.pub username@ip
```

📌 This command specifies which **public key** to send to the host machine. In turn, it will be added to `~/.ssh/authorized_keys`.

🔄 Alternatively, if you want to **automatically pick the default public key** from `~/.ssh/`, use:

```bash
ssh-copy-id username@ip
```

---

#### **4️⃣ Verify the Key on the Host Machine (Optional)**

🛠️ On your **host machine**, check if the key was copied successfully:

```bash
cat ~/.ssh/authorized_keys
```

The key in this file should be exactly the same as the public key on your client machine. If there are multiple keys, look for the one that matches your public key.

---

#### **5️⃣ Log in to the Host Machine from the Client Machine**

🔑 Now, try logging into your host machine from the client machine:

```bash
ssh username@ip
```

🔐 The **first attempt** will still ask for a password.  
🎉 On the **second attempt**, key-based authentication should work.

---

### **⚠️ Troubleshooting: Still Asking for Password?**

If SSH **still** prompts for a password after the first attempt:

1️⃣ On your **host machine**, edit the SSH configuration file:

```bash
sudo nvim /etc/ssh/sshd_config
```

2️⃣ 🔎 Search for the following settings and update them if necessary:

- **PasswordAuthentication** → Change `yes` to `no`
    
- **PublicKeyAuthentication** → Change `no` to `yes`
    
- **AuthorizedKeysFile** → Uncomment this line
    

3️⃣ 💾 Save and exit (`:wq` in `nvim`).

4️⃣ 🔄 Restart the SSH server:

```bash
sudo systemctl restart ssh
```

---

### **🎉 You're Done!**

✅ Now, you should be able to log in **without a password** using SSH key-based authentication. 🚀


publicip and wifi port forwarding
