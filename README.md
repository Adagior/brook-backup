# brook-backup
brook-backup

server
```
firewall-cmd --zone=public --permanent --add-port=9797/tcp
firewall-cmd --zone=public --permanent --add-port=9797/udp
systemctl restart firewalld.service

wget https://github.com/txthinking/brook/releases/download/v20190601/brook
chmod a+x brook
nohup ./brook ssserver -l :9797 -p password >/dev/null 2>&1 &
exit
```

windows .bat
```
@echo off  
start cmd /k C:\brook_windows_amd64.exe ssclient -l 127.0.0.1:2333 -i 127.0.0.1 -s 1.2.3.4:9797 -p password
```
