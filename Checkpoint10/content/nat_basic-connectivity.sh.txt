# to flush NAT tables


iptables -t nat -F


iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE

iptables -t nat -A PREROUTING -j LOG --log-prefix "PREROUTING: "

iptables -t nat -A POSTROUTING -j LOG --log-prefix "POSTROUTING: "

  # to allow other students to access APACHE server
iptables -t nat -A PREROUTING -p tcp --dport 1886 -j DNAT --to-destination 172.17.86.37:80

  # to allow other students to access MySQL server
iptables -t nat -A PREROUTING -p tcp --dport 1686 -j DNAT --to-destination 172.17.86.37:3306

  # to allow other students to access Linux server - SSH
iptables -t nat -A PREROUTING -p tcp --dport 1286 -j DNAT --to-destination 172.17.86.37:22

  # to allow other students to access IIS server
iptables -t nat -A PREROUTING -p tcp --dport 1986 -j DNAT --to-destination 172.17.86.36:80

  # to allow other students to access Windows server - RDP
iptables -t nat -A PREROUTING -p tcp --dport 1386 -j DNAT --to-destination 172.17.86.36:3389
