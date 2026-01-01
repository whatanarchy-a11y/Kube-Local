PS C:\Users\LG> wsl --install

PS C:\Users\LG> wsl --set-default-version 2

PS C:\Users\LG> wsl -l -v
  NAME      STATE           VERSION
* Ubuntu    Stopped         2

PS C:\Users\LG> wsl -d Ubuntu
root@DESKTOP-D6A344Q:/mnt/c/Users# sudo tee /etc/wsl.conf >/dev/null <<'EOF'
[boot]
systemd=true
EOF

root@DESKTOP-D6A344Q:/mnt/c/Users# sudo apt update
root@DESKTOP-D6A344Q:/mnt/c/Users# sudo apt -y upgrade

root@DESKTOP-D6A344Q:/mnt/c/Users# exit
logout

PS C:\Users\LG> wsl --shutdown

PS C:\Users\LG> systemctl is-system-running

PS C:\Users\LG> wsl -d Ubuntu

root@DESKTOP-D6A344Q:/mnt/c/Users/LG# systemctl is-system-running
running

root@DESKTOP-D6A344Q:/mnt/c/Users/LG# sudo nano /etc/wsl.conf
[boot]
systemd=true
