When maintaining a Linux server, regularly reviewing auth logs is crucial. These logs record all authentication-related activities such as system logins, password changes, and sudo commands.

### **Log Locations**

- **Debian-based systems**: `/var/log/auth.log`
    
- **Red Hat & CentOS**: `/var/log/secure`
    

### **Importance of Auth Logs**

- Detect brute-force login attempts
    
- Identify unauthorized access
    
- Monitor suspicious activity
    
- Ensure server security and data integrity
    

### **View Auth Logs in Real Time**

To continuously monitor authentication logs, use:

```sh
sudo tail -f /var/log/auth.log
```

For Red Hat & CentOS:

```sh
sudo tail -f /var/log/secure
```

`-f` flag is the follow command
### **Example Auth Log Entries**

Below is an example of authentication logs from a system:

```
2025-03-29T10:40:04 pkexec: session opened for user root by gautam
2025-03-29T10:40:04 pkexec: gautam executed a command as root
2025-03-29T10:45:01 CRON: session opened for user root
2025-03-29T10:45:01 CRON: session closed for user root
2025-03-29T10:51:35 systemd-logind: Watching system buttons
2025-03-29T10:55:01 CRON: session opened for user root
2025-03-29T10:55:01 CRON: session closed for user root
2025-03-29T11:05:01 CRON: session opened for user root
2025-03-29T11:05:01 CRON: session closed for user root
```

### **Understanding Auth Log Entries**

- **pkexec**: A process was executed with elevated privileges.
    
- **CRON**: Scheduled jobs ran as the root user.
    
- **systemd-logind**: The system detected hardware input changes.
    

### **Dropbear vs OpenSSH Logging**

Unlike OpenSSH, which logs authentication events in `/var/log/auth.log`, **Dropbear** handles logging differently. Dropbear logs authentication events directly to system logs and may require using `journalctl` or checking `/var/log/syslog` instead. To monitor Dropbear logs, use:

```sh
sudo journalctl -f -u dropbear
```

### **Recent Dropbear Log Entries**

```
Mar 29 11:23:21 dropbear[5032]: Exit (gautam) from 49.35.194.238:44478: Exited normally
Mar 29 11:23:25 dropbear[5357]: Child connection from 49.35.194.85:44536
Mar 29 11:23:34 dropbear[5357]: Password auth succeeded for 'gautam' from 49.35.194.85:44536
Mar 29 11:24:07 sudo[5417]: gautam ran 'ls' as root
Mar 29 11:24:07 sudo[5417]: session opened for root by gautam
Mar 29 11:24:07 sudo[5417]: session closed for root
Mar 29 11:24:17 dropbear[5357]: Exit (gautam) from 49.35.194.85:44536: Exited normally
Mar 29 11:25:34 dropbear[5456]: Child connection from 162.243.198.177:53786
Mar 29 11:25:35 dropbear[5456]: Exit before auth from 162.243.198.177:53786: (user 'root', 0 fails): Exited normally
```

### **Analysis of Dropbear Logs**

- **Successful login**: Gautam logged in successfully from `49.35.194.85`.
    
- **Sudo command**: Gautam ran `ls` as root and the session was opened and closed properly.
    
- **Connection attempts**:
    
    - A connection was made from `162.243.198.177`, but it exited before authentication, possibly an automated scan or failed attempt.
        

### **Understanding Journalctl Flags**

- `-u` (unit): Specifies the service unit to monitor.
    
- `-f` (follow): Continuously outputs new log entries as they appear.
    

Note: `journalctl` does not support combining `-f` and `-u` as `-fu` or `-uf`. The correct format is:

```sh
sudo journalctl -f -u dropbear
```

Regularly analyzing these logs helps in identifying any unusual activity and maintaining security.