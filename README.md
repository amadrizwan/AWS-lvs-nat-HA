# AWS-lvs-nat-HA

a script that runs on monitor instance and provide high availability to LVS and NAT instances.

Limitations:

Both LVS instances should be in the same Availability Zone. That is because a secondary IP address can only be reassociated within the same subnet.


The secondary IP address can be configured on both LVS instances at the same time.

CENTOS:
vi /etc/sysconfig/network-scripts/ifcfg-eth0:1
DEVICE=eth0:1
BOOTPROTO=static
ONBOOT=yes
IPADDR=172.31.50.100
NETMASK=255.255.255.0
ARPCHECK=no
