# perform intial switch config. 
## access the switch cli and - 
Switch>enable
Switch#configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
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

