# How to create and use free vpn on AWS 

## Steps 
1. Create a free tier  AWS account
2. Click all services
3. Click  EC2
4. Go to instances
5. Launch instances
6. Name your server i named as openVPN
7. In Application and OS Images click browse more AMIs (Amazon Machine Images)
8. search for openvpn and the first one is the correct one for free tier subscribe it
9. In instance type make sure you are selected the free tier eligble
10. create a keypair login this step is very important because you are going to ssh with this pair
11. click launch instance. All done!!
12. ssh -i "keypairVPN.pem" openvpnas@ec2-10.10.10.10.eu-north-1.compute.amazonaws.com  aws is going to give you this and you need to open powershell and paste this
13. default is fine, just enter it but make sure when the password section come up put a very secure password
14. Go back to aws dashboard and copy your public IPv4 address
15. 10.10.10.10:943/admin your username will be openvpn and the password you created in step 13
16. go to the vpn settings
17. in routing make sure should client internet traffic be routed through the vpn? is yes. save it.
18. go to 10.10.10.10:943 this site and download the gui
19. all done you are know connect through vpn. But after you finished make sure you stop EC2 instance 
