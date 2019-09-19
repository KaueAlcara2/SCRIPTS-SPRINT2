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


SW
mostre o vlan breve
vlan 10
nome RH
interface fastethernet 0/1
acesso switchport vlan 10
acesso ao modo switchport
fim
vlan 20
nome ADM
interface fastethernet 0/2
acesso switchport vlan 20
acesso ao modo switchport
fim
vlan 30
nome QUALIDADE
interface fastethernet 0/3
acesso switchport vlan 30
acesso ao modo switchport
fim
vlan 40
nome RECEPCAO
interface fastethernet 0/4
acesso switchport vlan 40
acesso ao modo switchport
fim
vlan 50
nome TI
interface fastethernet 0/5
acesso switchport vlan 50
acesso ao modo switchport
fim
vlan 60
nome ANALISTAS
interface fastethernet 0/6
acesso switchport vlan 60
acesso ao modo switchport
fim
vlan 70
nome FINANCIAS
interface fastethernet 0/7
acesso switchport vlan 70
acesso ao modo switchport
fim
vlan 80
nome CONSULTORES
interface fastethernet 0/8
acesso switchport vlan 80
acesso ao modo switchport
fim
vlan 90
nome VOZ
interface fastethernet 0/9
acesso switchport vlan 90
acesso ao modo switchport
fim
-----------------------------------
interface fastethernet0 / 1
switchport tronco nativo vlan 99
tronco de switchport permitido vlan 10,20,30,99
fim
(REPETE PARA TODAS AS OUTRAS)
-----------------------------------
