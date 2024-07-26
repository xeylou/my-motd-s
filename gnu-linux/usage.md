1. paste the content of [banner.txt](https://github.com/xeylou/my-motd-s/blob/main/gnu-linux/banner.txt) into `/etc/ssh/banner`
2. modify the ssh properties to use the file as a banner and prevent showing the latest connection info
```conf
#[...]
Banner /etc/ssh/banner
#[...]
PrintLastLog no
```
3. paste the files of [update-motd.d](https://github.com/xeylou/my-motd-s/blob/main/gnu-linux/update-motd.d) into your `/etc/update-motd.d/` folder
4. make sure they are executable `chmod 755 /etc/update-motd.d/*`
5. `apt install -y figlet bc`