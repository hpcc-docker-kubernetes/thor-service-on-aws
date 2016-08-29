# Demo of Docker/Kubernetes on AWS
r-service-on-aws
Will demostrate set thor ip with kubernetes service which will not change when the thor is restarted/recreated. We already make roxie and esp behind load balancers and environemnt.xml only has load balancers for others HPCC nodes. There are three shared environment on NFS file server: roxie, esp and dali/thor/support node. For roxie and esp it has localhost for local component in their environemnt.xml

# This still does not work
## Thor start hang
## Even thor started (without dafilesrv) playground sample fails: 
'''sh
00000018 2016-08-29 17:01:22.129  2609  2609 "Registration confirmation from 10.0.188.179:20100"
00000019 2016-08-29 17:01:22.129  2609  2609 "Slave 1 (10.0.188.179:20100) registered"
0000001A 2016-08-29 17:06:00.165  2609  2622 "Watchdog : Unknown Machine! [10.244.1.5:20100]"
0000001B 2016-08-29 17:06:01.167  2609  2609 "ERROR: 4: /var/lib/jenkins2/workspace/CE-Candidate-6.0.4-1/CE/ubuntu-14.04-amd64/HPCC-Platform/thorlcr/master/thmastermain.cpp(323) : Slave registration exception : MP link closed (10.0.209.49:20100)"
0000001C 2016-08-29 17:06:21.168  2609  2609 "Timeout waiting for Shutdown reply from slave(s) (0 replied out of 1 total)"
0000001D 2016-08-29 17:06:21.168  2609  2609 "Slaves that have not replied: 1"
0000001E 2016-08-29 17:06:21.168  2609  2609 "Registration aborted"
0000001F 2016-08-29 17:06:21.168  2609  2609 "ThorMaster terminated OK"

'''
