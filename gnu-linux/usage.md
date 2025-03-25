1. modify and paste the content of [banner.txt](https://github.com/xeylou/my-motd-s/blob/main/gnu-linux/banner.txt) to `/etc/ssh/banner`
2. modify the ssh properties to use the file as a banner and prevent ssh from showing the latest connection info
```conf
#[...]
Banner /etc/ssh/banner
#[...]
PrintLastLog no
```
3. paste the files from [update-motd.d](https://github.com/xeylou/my-motd-s/blob/main/gnu-linux/update-motd.d) to your `/etc/update-motd.d/` folder
4. make sure they are executable except the unnecessary ones `chmod 755 [0-3]*`
5. dependencies `apt install -y figlet bc`
6. (optional) test/troubleshoot `run-parts /etc/update-motd.d/ > /dev/null`
