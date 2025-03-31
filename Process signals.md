process signals are the signals that are used to control a process
1.
- In **Bash**, `kill -l` lists all signal names.
    
- In **Zsh**, `kill -l` only prints the signals up to **SIGSYS**, excluding real-time signals.

suppose a process runs in the foreground like
- sleep 14568 and then ctrl+z
 suppose a process runs in the background like
 - sleep 666 & (immediately sent to background)

To stop a process  we can use the command kill -SIGTSTP PID
sometimes the process can be ignored when we do sigtstp,in that case use 
SIGSTOP





