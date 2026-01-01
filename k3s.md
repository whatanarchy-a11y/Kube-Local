root@DESKTOP-D6A344Q:/mnt/c/Users/LG# curl -sfL https://get.k3s.io | sh -
sudo systemctl status k3s

root@DESKTOP-D6A344Q:/mnt/c/Users/LG# vi /etc/rancher/k3s/k3s.yaml

root@DESKTOP-D6A344Q:/mnt/c/Users/LG# sudo cat /var/lib/rancher/k3s/server/node-token
K10c41db8ef6e897dd980e6aeb09f6be57b65d38e4bb84c9e8e89b64aa555af4db6::server:aad47024f2fb3a0d24423334a72a586c


root@DESKTOP-D6A344Q:/mnt/c/Users/LG# apt install net-tools

root@DESKTOP-D6A344Q:/mnt/c/Users/LG# ip -br a
lo               UNKNOWN        127.0.0.1/8 10.255.255.254/32 ::1/128
eth0             UP             172.22.95.21/20 fe80::215:5dff:feba:bf00/64
flannel.1        UNKNOWN        10.42.0.0/32 fe80::3424:8dff:fec2:bc2f/64
cni0             UP             10.42.0.1/24 fe80::8472:2ff:fee4:2463/64
veth001af001@if2 UP             fe80::94d1:f9ff:fe59:8d14/64
vethf14fc0e6@if2 UP             fe80::4496:42ff:fed6:7fd2/64
veth8b3fc7b6@if2 UP             fe80::68de:20ff:fe25:4d2c/64
veth7e0e71b8@if2 UP             fe80::e475:c9ff:fee6:48db/64
vetha16d619d@if2 UP             fe80::18d4:b2ff:fe1b:4247/64


sudo apt update
sudo apt install -y iptables iptables-persistent conntrack socat ebtables ethtool


command -v iptables-save
command -v iptables-restore


sudo update-alternatives --set iptables /usr/sbin/iptables-legacy
sudo update-alternatives --set ip6tables /usr/sbin/ip6tables-legacy


curl -sfL https://get.k3s.io | K3S_URL=https://192.168.56.10:6443 K3S_TOKEN=K10c41db8ef6e897dd980e6aeb09f6be57b65d38e4bb84c9e8e89b64aa555af4db6::server:aad47024f2fb3a0d24423334a72a586c sh -

curl -sfL https://get.k3s.io | \
  K3S_URL="https://192.168.56.10:6443" \
  K3S_TOKEN="K10c41db8ef6e897dd980e6aeb09f6be57b65d38e4bb84c9e8e89b64aa555af4db6::server:aad47024f2fb3a0d24423334a72a586c" \
  sh -s - --node-ip 192.168.56.11 --flannel-iface enp0s8
