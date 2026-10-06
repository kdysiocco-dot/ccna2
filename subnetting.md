
 
 
@D1
config t
vlan 20
name ACCENTURE
Interface vlan 20
 desc ACCENTURE.com
 no shut
ip add 10.0.0.129 255.255.255.128 
ip dhcp excluded-add 10.0.0.129 10.0.0.139
ip dhcp pool ACCENTURE.com
 network 10.0.128.0 255.255.255.128
 default-router 10.0.0.129
 Domain-name ACCENTURE.COM
 
 INT E1/0
 NO SH
 SWITCHPORT MODE ACCESS
 SWITchport access vlan 20
 
 @s1
 config t
 int e1/0
 no shut
 ip add dhcp
 do bp
 
@C1 
config t
vlan 21
name CHEVRON
Interface vlan 21
 desc CHEVRON.com
 no shut
ip add 10.0.8.1 255.255.248.0 
NO ip dhcp excluded-add 10.0.8.1 10.0.0.100
ip dhcp excluded-add 10.0.8.1 10.0.8.100
ip dhcp pool CHEVRON.com
 network 10.0.8.0 255.255.248.0
 default-router 10.0.8.1
 Domain-name CHEVRON.COM
 
 
 @A1
 INT E0/0
 NO SH
 SWITCHPORT MODE ACCESS
 SWITchport access vlan 21
 DO SHOW VLAN BRIEF
 @P1
 config t
 int e0/0
 no shut
 ip add dhcp
 do bp
 
@C1 
config t
vlan 22
name SHELL
Interface vlan 22
 desc SHELL.com
 no shut
ip add 10.0.16.1 255.255.240.0 
ip dhcp excluded-add 10.0.16.1 10.0.16.100
ip dhcp pool SHELL.com
network 10.0.16.0 255.255.240.0
default-router 10.0.16.1
Domain-name SHELL.COM

 @A2
 INT E1/0
 NO SH
 SWITCHPORT MODE ACCESS
 SWITchport access vlan 23
 DO SHOW VLAN BRIEF
 
  @P2
config t
int e1/0
 no shut
 ip add dhcp
 do bp
 
 @C1 
config t
vlan 23
name FUELSAVE
Interface vlan 23
 desc FUELSAVE.com
 no shut
ip add 10.0.2.1 255.255.254.0 
ip dhcp excluded-add 10.0.2.1 10.0.2.100
ip dhcp pool FUELSAVE.com
network 10.0.2.0 255.255.254.0
default-router 10.0.2.1
Domain-name FUELSAVE.COM
