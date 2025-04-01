- [x] 1.file compression (done)
- [x] 2.copying and renaming
- [x] 3.soft link and hardlink
- [x] 4.uptime
- [x] 5.authlog
- [x] 6.services running
- [ ] 7.available memory disks
- [ ] 8.bg/fg process
- [ ] 9.listing and finding processes
to make notes on ssh keygeneration
#doubt
to kill an sftp server, 
like sudo lsof -i :22 - to get pid

sudo kill -9 pid
or sudo pkill -9 sshd or sudo pkill -9 -f sftp-server
#askInReddit 
when i kill it shows connection refused, and then still it seems as if i am logged into it
when i hit enter, again the prompt appear, again i hit enter, again it appears and during the third time, it gets exited finally , why is it so?
i even masked using the command "sudo systemctl mask ssh.socket"

