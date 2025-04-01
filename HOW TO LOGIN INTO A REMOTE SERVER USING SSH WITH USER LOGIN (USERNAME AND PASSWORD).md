# 🖥️ HOW TO LOGIN INTO A REMOTE SERVER USING SSH WITH USER LOGIN (USERNAME AND PASSWORD)

## 🔹 Step 1: Install Required Packages

📥 Install **OpenSSH Server** (for self-hosting your Linux distro) or **Dropbear** (a lightweight SSH server and client).

To install OpenSSH Server:
- **Debian/Ubuntu:**
  ```bash
  sudo apt install openssh-server -y
  ```
- **Arch Linux:**
  ```bash
  sudo pacman -S openssh
  ```
- **Fedora:**
  ```bash
  sudo dnf install openssh-server
  ```
- **CentOS/RHEL:**
  ```bash
  sudo yum install -y openssh-server
  ```

🔹 **Note:** For Dropbear, replace `openssh-server` with `dropbear` in the installation commands.

---

## 🔹 Step 2: Check SSH Server Status

🛠️ Run the following command to check the status:

- If you are using **Dropbear**:
  ```bash
  sudo systemctl status dropbear
  ```
- If you are using **OpenSSH Server**:
  ```bash
  sudo systemctl status ssh
  ```

⚡ In the further steps, we will continue with **OpenSSH**. Everything will be the same for **Dropbear**.

---

## 🔹 Step 3: Start the SSH Server (If Inactive)

🚀 If the status shows **inactive**, start the server using:
  ```bash
  sudo systemctl start ssh
  ```
_(Replace "start" with "stop" to stop the server.)_

---

## 🔹 Step 4: Open a Terminal for Connection

🖥️ Open a **new terminal**, the **previous terminal**, **PuTTY**, **Termux**, or any other terminal to connect to the host computer.

---

## 🔹 Step 5: Find the Host's IP and Username

🌐 To get the **IP address**, run:
  ```bash
  ifconfig
  ```
🔍 Search for **"inet"**—the digits following the colon are the **user’s IP(private)**.

👤 To get the **username**, run:
  ```bash
  whoami
  ```

📌 **Note:**
- If the **client and host are on the same network** (e.g., same WiFi router), use the **local IP** to connect.
- If the **client and host are on different networks** (e.g., the host is on home WiFi and the client is on cellular data or different WiFi), use the **public IP** of the host. Get it by visiting [WhatIsMyIP.com](https://www.whatismyip.com/) on the **host machine**.
- **Ensure port forwarding for port 22** on your **host machine’s WiFi router** to allow the connection.
- **Ignore port forwarding if on the same network**, as you can directly connect using the host machine’s private IP.

---
**Note:** My host is connected to a WiFi router, and my client machine (phone) is on a cellular network, so I need to consider my public IP.
## 🔹 Step 6: Connect to the Remote Server

🔑 Run the following command:
  ```bash
ssh username@ip
  ```
🔐 You will be asked for a **password** to run the `sudo` command and another **password** to log into the server.

---

## 🔹 Step 7: Log into the Server

💻 Now, connect to the server using the command from **Step 6**, replacing it with the host’s **username** and **IP**, then enter the **password**.

---

## 🔹 Step 8: Verify the SSH Connection

🔍 To check if the connection is active, run:
  ```bash
  who
  ```
📋 It will show a **list of users** currently using your distro.
Look for something like **/pts/0** or **/pts/any_number**—if it's present, your session is **active**, or a user is **logged in**.

---

## 🔹 Step 9: Kill an Active SSH Connection (If Needed)

⚠️ To **terminate** a particular SSH session, run:
  ```bash
  sudo fuser -k /dev/pts/<the_number>
  ```
🔌 This will **disconnect** the user from the SSH session.

---

## 🔹 Step 10: Confirm Disconnection

🔁 Again, check the **active connections** using the `who` command.

---

## 🔹 Step 11: Logout or Stop the SSH Server

🔓 To **log out**, type:
  ```bash
  exit
  ```
⛔ To **stop the SSH server**, run the command listed in **Step 2**.

