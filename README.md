# How to create and use free vpn on AWS 

## Steps 
1. Create a free tier  AWS account
2. Click all services
   ![alt text](https://github.com/wiemBe/How-to-VPN/blob/main/src/s7.png)
4. Click  EC2
5. Go to instances
6. Launch instances
7. Name your server i named as openVPN
8. In Application and OS Images click browse more AMIs (Amazon Machine Images)
9. search for openvpn and the first one is the correct one for free tier subscribe it
10. In instance type make sure you are selected the free tier eligble
11. create a keypair login this step is very important because you are going to ssh with this pair
12. click launch instance. All done!!
13. ssh -i "keypairVPN.pem" openvpnas@ec2-10.10.10.10.eu-north-1.compute.amazonaws.com  aws is going to give you this and you need to open powershell and paste this
14. default is fine, just enter it but make sure when the password section come up put a very secure password
15. Go back to aws dashboard and copy your public IPv4 address
16. 10.10.10.10:943/admin your username will be openvpn and the password you created in step 13
17. go to the vpn settings
18. in routing make sure should client internet traffic be routed through the vpn? is yes. save it.
19. go to 10.10.10.10:943 this site and download the gui
20. all done you are know connect through vpn. But after you finished make sure you stop EC2 instance 
