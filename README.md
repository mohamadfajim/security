````
ufw allow 1000:1999/tcp
ufw allow 1000:1999/udp
ufw allow 22/tcp
ufw allow 22/udp
ufw enable

````


````
sudo iptables -I OUTPUT -s 1.2.3.0/24 -j DROP
sudo iptables -I OUTPUT -s 102.91.14.0/23 -j DROP
sudo iptables -I OUTPUT -s 102.91.16.0/20 -j DROP
sudo iptables -I OUTPUT -s 123.44.0.0/15 -j DROP
sudo iptables -I OUTPUT -s 200.0.0.0/8 -j DROP
sudo iptables -I OUTPUT -s 102.0.0.0/8 -j DROP
sudo iptables -I OUTPUT -s 10.0.0.0/8 -j DROP
sudo iptables -I OUTPUT -s 100.64.0.0/10 -j DROP
sudo iptables -I OUTPUT -s 169.254.0.0/16 -j DROP
sudo iptables -I OUTPUT -s 198.18.0.0/15 -j DROP
sudo iptables -I OUTPUT -s 198.51.100.0/24 -j DROP
sudo iptables -I OUTPUT -s 203.0.113.0/24 -j DROP
sudo iptables -I OUTPUT -s 224.0.0.0/4 -j DROP
sudo iptables -I OUTPUT -s 240.0.0.0/4 -j DROP
sudo iptables -I OUTPUT -s 255.255.255.255/32 -j DROP
sudo iptables -I OUTPUT -s 192.0.0.0/24 -j DROP
sudo iptables -I OUTPUT -s 192.0.2.0/24 -j DROP
sudo iptables -I OUTPUT -s 127.0.53.53 -j DROP
sudo iptables -I OUTPUT -s 192.168.0.0/16 -j DROP
sudo iptables -I OUTPUT -s 0.0.0.0/8 -j DROP
sudo iptables -I OUTPUT -s 224.0.0.0/3 -j DROP
sudo iptables -I OUTPUT -s 192.88.99.0/24 -j DROP
sudo iptables -I OUTPUT -s 169.254.0.0/16 -j DROP
sudo iptables -I OUTPUT -s 198.18.140.0/24 -j DROP
sudo iptables -I OUTPUT -s 1.2.3.0/24 -j DROP
sudo iptables -I OUTPUT -s 102.91.14.0/23 -j DROP
sudo iptables -I OUTPUT -s 102.91.16.0/20 -j DROP
sudo iptables -I OUTPUT -s 123.44.0.0/15 -j DROP
sudo iptables -I OUTPUT -s 102.0.0.0/8 -j DROP
sudo iptables -I OUTPUT -s 198.18.0.0/15 -j DROP

````

````
sudo iptables -A OUTPUT -o eth0 -d 0.0.0.0/8 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 10.0.0.0/8 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 100.64.0.0/10 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 127.0.0.0/8 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 169.254.0.0/16 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 172.16.0.0/12 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 192.0.2.0/24 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 192.168.0.0/16 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 198.18.0.0/15 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 224.0.0.0/4 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 240.0.0.0/4 -j DROP
sudo iptables -A OUTPUT -o eth0 -d 203.0.113.0/24 -j DROP 
sudo iptables -A OUTPUT -o eth0 -d 224.0.0.0/3 -j DROP 
sudo iptables -A OUTPUT -o eth0 -d 198.51.100.0/24 -j DROP 
sudo iptables -A OUTPUT -o eth0 -d 192.88.99.0/24 -j DROP 
sudo iptables -A OUTPUT -o eth0 -d 192.0.0.0/24 -j DROP
iptables -A OUTPUT -o eth0 -d 223.202.0.0/16 -j DROP
iptables -A OUTPUT -o eth0 -d 194.5.192.0/19 -j DROP
iptables -A OUTPUT -o eth0 -d 209.237.192.0/18 -j DROP
iptables -A OUTPUT -o eth0 -d 169.254.0.0/16 -j DROP

````


````
iptables -A OUTPUT -p tcp -s 0/0 -d 10.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 100.64.0.0/10 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 10.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 100.64.0.0/10 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 141.101.78.0/23 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 173.245.48.0/20 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.0.2.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 141.101.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 141.101.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 173.245.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 173.245.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d  10.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 10.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 100.64.0.0/10 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 100.64.0.0/10 -j DROP

````

````
iptables-save

````


