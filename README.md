````
ufw allow 22/tcp
ufw allow 22/udp
ufw allow 2053/tcp
ufw allow 2053/udp
ufw allow 443/tcp
ufw allow 443/udp
ufw allow 80/tcp
ufw allow 80/udp
ufw enable

````

````
ufw deny out from any to 10.0.0.0/8
ufw deny out from any to 172.16.0.0/12
ufw deny out from any to 192.168.0.0/16
ufw deny out from any to 100.64.0.0/10
ufw deny out from any to 198.18.0.0/15
ufw deny out from any to 169.254.0.0/16
ufw deny out from any to 173.245.0.0/16
ufw deny out from any to 141.101.0.0/16
ufw deny out from any to 151.139.128.9
ufw deny out from any to 205.185.208.153
ufw deny out from any to 192.0.0.0/24
ufw deny out from any to 1.2.3.0/24
ufw deny out from any to 102.91.14.0/23
ufw deny out from any to 123.44.0.0/15
ufw deny out from any to 200.0.0.0/8
ufw deny out from any to 198.51.100.0/24
ufw deny out from any to 203.0.113.0/24
ufw deny out from any to 224.0.0.0/4
ufw deny out from any to 255.255.255.255/32
ufw deny out from any to 192.0.2.0/24
ufw deny out from any to 127.0.53.53
ufw deny out from any to 0.0.0.0/8
ufw deny out from any to 224.0.0.0/3
ufw deny out from any to 198.18.140.0/24
ufw deny out from any to 102.91.16.0/20
ufw deny out from any to 102.0.0.0/8
ufw deny out from any to 127.0.0.0/8
ufw deny out from any to 240.0.0.0/4
ufw deny out from any to 223.202.0.0/16
ufw deny out from any to 194.5.192.0/19
ufw deny out from any to 209.237.192.0/18
ufw deny out from any to 141.101.78.0/23
ufw deny out from any to 173.245.48.0/20
ufw deny out from any to 151.139.128.10
ufw deny out from any to 192.0.0.1/24

````

````
ufw enable

````

````
iptables -A OUTPUT -p tcp -s 0/0 -d 10.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 100.64.0.0/10 DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 198.18.0.0/15 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 169.254.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 173.245.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 141.101.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 151.139.128.9 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 205.185.208.153 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.0.0.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 1.2.3.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 102.91.14.0/23 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 123.44.0.0/15 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 200.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 198.51.100.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 203.0.113.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 224.0.0.0/4 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 255.255.255.255/32 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.0.2.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 127.0.53.53 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 0.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 224.0.0.0/3 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 198.18.140.0/24 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 102.91.16.0/20 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 102.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 127.0.0.0/8 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 240.0.0.0/4 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 223.202.0.0/16 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 194.5.192.0/19 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 209.237.192.0/18 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 141.101.78.0/23 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 173.245.48.0/20 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 151.139.128.10 -j DROP
iptables -A OUTPUT -p tcp -s 0/0 -d 192.0.0.1/24 -j DROP

````

````
iptables -A OUTPUT -p udp -s 0/0 -d 10.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 172.16.0.0/12 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.168.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 100.64.0.0/10 DROP
iptables -A OUTPUT -p udp -s 0/0 -d 198.18.0.0/15 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 169.254.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 173.245.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 141.101.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 151.139.128.9 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 205.185.208.153 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.0.0.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 1.2.3.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 102.91.14.0/23 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 123.44.0.0/15 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 200.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 198.51.100.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 203.0.113.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 224.0.0.0/4 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 255.255.255.255/32 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.0.2.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 127.0.53.53 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 0.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 224.0.0.0/3 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 198.18.140.0/24 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 102.91.16.0/20 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 102.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 127.0.0.0/8 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 240.0.0.0/4 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 223.202.0.0/16 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 194.5.192.0/19 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 209.237.192.0/18 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 141.101.78.0/23 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 173.245.48.0/20 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 151.139.128.10 -j DROP
iptables -A OUTPUT -p udp -s 0/0 -d 192.0.0.1/24 -j DROP

````

````
iptables-save

````
