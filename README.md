# perform intial switch config. 
## access the switch cli and - 
Switch>enable

Switch#configure terminal

Switch(config)#hostname s1

s1(config)#enable secret class123

s1(config)#line console 0

s1(config-line)#password cisco

s1(config-line)#login

s1(config-line)#exit

s1(config)#line vty 0 15

s1(config-line)#password cisco 

s1(config-line)#login

s1(config-line)#exit

s1(config)#banner motd #Unauthorized Access Prohibited#

s1(config)#interface vlan 1

s1(config-if)#ip address 192.168.1.1 255.255.255.0

s1(config-if)#no shutdown

s1(config-if)#exit

s1(config)#exit

s1#copy running-config startup-config

Destination filename [startup-config]? { press enter}

Building configuration...
[OK]


# perform intial switch config.  
## access the router cli and -
Router> enable

Router# configure terminal

Router (config)# hostname R1

R1 (config)# enable secret class123

R1 (config)# line console 0

R1 (config-line)# password cisco

R1 (config-line)# login

R1 (config-line)# exit

R1 (config)# line vty 0 15

R1 (config-line)# password cisco

R1 (config-line)# login

R1 (config-line)# exit

R1 (config)# banner motd #Authorized Access Only#

R1 (config)# interface gigabitEthernet 0/0

R1 (config-if)# ip address 192.168.1.1 255.255.255.0

R1 (config-if)# no shutdown

R1(config-if)# exit

R1 (config)# exit

then to Save the configuration:

S1# copy running-config startup-config

Destination filename [startup-config]? { press enter}

Building configuration...
[OK]

# To Implement Connection Between Devices Using router 
## give ips to pcs and router and ACCESS THE ROUTER CLI- 

Left network PCs: 

PC1 → 192.168.1.2

PC2 → 192.168.1.3

Right network PCs:

PC3 → 192.168.2.2

PC4 → 192.168.2.3

Router(config-if)#

Router#

Router#config

Configuring from terminal, memory, or network [terminal]? terminal

Enter configuration commands, one per line. End with CNTL/2.

Router(config)#interface g0/0

Router (config-if)#ip address 192.168.1.11 255.255.255.0

Router(config-if)#no shutdown

Router(config-if)#exit

Router(config-if)#

Router#

Router#config

Configuring from terminal, memory, or network [terminal]? terminal Enter configuration commands, one per line. End with CNTL/Z.

Router(config)#interface g0/1

Router (config-if)#ip address 192.168.2.10 255.255.255.0

Router (config-if)#no shutdown

Router (config-if)#exit

Router (config)#
