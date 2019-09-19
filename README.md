SCRIPT ROUTER
configure terminal
hostname R1
banner motd "ACESSO APENAS PARA O DEPARTAMENTO DE T.I"
enable secret SenhaEnable
line console 0
password SenhadaConsole
login
exit
line vty 0 15
password SenhadaVTY
login
exit
service password-encryption
user
interface gigabitEthernet 0/0.10 
ip address 172.16.18.10 255.255.255.128
no shutdown
exi
interface gigabitEthernet 0/0.20
ip address 172.16.18.138 255.255.255.128
no shutdown
do wr 
interface gigabitEthernet0/0.30 
ip address 172.16.20.10 255.255.255.240
no shutdow
do wr
interface gigabitEthernet0/0.40 
ip address 172.16.19.202 255.255.255.192
no shutdow
do wr
interface gigabitEthernet0/0.50
ip address 172.16.19.138 255.255.255.192
no shutdow
do wr
interface gigabitEthernet0/0.60 
ip address 172.16.16.10 255.255.254.0
no shutdow
do wr
interface gigabitEthernet0/0.70
ip address 172.16.19.10 255.255.255.128
no shutdow
do wr
interface gigabitEthernet0/0.80
ip address 172.16.8.10 255.255.248.0
no shutdow
do wr
interface gigabitEthernet0/0.90 
ip address 172.16.0.10 255.255.248.0
no shutdow
do wr




