# ⚙️ Systemctl Command Reference

## 🔧 Managing Services

### ✅ Check Service Status

```bash
sudo systemctl status <service_name>
```

- 📌 Displays the current status of a service.
    

### ▶️ Start a Service

```bash
sudo systemctl start <service_name>
```

- 🚀 Starts a service immediately.
    

### ⏹️ Stop a Service

```bash
sudo systemctl stop <service_name>
```

- ❌ Stops a running service.
    

### 🔄 Restart a Service

```bash
sudo systemctl restart <service_name>
```

- 🔁 Restarts a service if it is running.
    

### 🔗 Enabling a Service

```bash
sudo systemctl enable <service_name>
```

- ⚡ Ensures the service starts on boot.
    
- ⚠️ Does not start the service immediately.
    
- 🔑 Requires admin rights.
    

### 🚀 Enable and Start a Service Simultaneously

```bash
sudo systemctl enable --now <service_name>
```

### 🔍 Check if a Service is Enabled

```bash
sudo systemctl is-enabled <service_name>
```

### 🚫 Disable a Service

```bash
sudo systemctl disable <service_name>
```

- ❎ Disables the service from starting on boot.
    
- ⚙️ The service can still be started manually.
    

### 🔒 Prevent a Service from Starting

```bash
sudo systemctl mask <service_name>
```

### 🔓 Allow a Service to Start

```bash
sudo systemctl unmask <service_name>
```

### 🔓 To list all the services

```bash
systemctl list-units --type=service
```

## 🔌 Working with Sockets

### 📡 List Available IPC Sockets

```bash
systemctl list-sockets
```

### 🔎 Show Socket Types

```bash
systemctl --show-types list-sockets
```

### 🎯 Show Specific Socket Type

```bash
systemctl --show-types list-sockets 'systemd*'
```

### 🗂️ Show All Socket Types

```bash
systemctl --show-types list-sockets --all
```

### 📋 List Running Services

```bash
systemctl | grep -i Running
```

## 📜 Viewing System Logs

### 📝 View Logs of a Specific Service

```bash
sudo journalctl -u <service_name>
```

### 🔄 View Logs from the Last Boot

```bash
sudo journalctl -b
```

### ⏳ View Logs in Real-time

```bash
sudo journalctl -f
```

### 🔍 View Real-time Logs of a Particular Service

```bash
sudo journalctl -f -u <service_name>
```

### ⏰ View Logs Since a Specific Date

```bash
journalctl -u <service_name> --since "YYYY-MM-DD HH:MM:SS"
journalctl -u <service_name> --since today
```

## 🛑 System Shutdown Commands

### 🔌 Power Off the System

```bash
systemctl poweroff
```

### 🔄 Reboot the System

```bash
systemctl reboot
```

### ⚠️ Force Reboot (Ignoring Logged-in Users)

```bash
systemctl -i reboot
```

### ⏳ Schedule a Shutdown

```bash
sudo shutdown -h +30
```

- ⏰ Shuts down the system in 30 minutes.
    

### ❌ Cancel a Scheduled Shutdown

```bash
sudo shutdown -c
```