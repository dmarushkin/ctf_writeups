# ServMon Box white-up


Nmap scan:

![](https://i.imgur.com/fgPxI9G.jpg)

No login for FTP: 

![](https://i.imgur.com/zvmbcpH.png)

Two users found:
 - Nadine
 - Nathan

And we found two files:
  - /Users/Nadine/Confidencial.txt
  - /Users/Nathan/Notes to do.txt

![](https://i.imgur.com/GaZPfTZ.png)


TVT NVMS-1000 Video capturing service on http://10.10.10.184/Pages/login.htm

![](https://i.imgur.com/dxf3bPV.png)

Service is vulnerable to Directory traversal (https://www.exploit-db.com/exploits/47774) so we can try to access /users/nathan/desktop/Passwords.txt

![](https://i.imgur.com/OqQ9Awg.png)


We try Nathan and nadine with this password in msf scanner/smb/smb_login:

![](https://i.imgur.com/CATEbcF.png)

And got nadine:Lxxxxxxxxxrk valid creds!

It works for SSH and we got user's flag:

![](https://i.imgur.com/IDXMVqa.png)



NSClient++ on https://10.10.10.184:8443/index.html#

![](https://i.imgur.com/GCT8HOC.png)

Service has privelage escalation vulnerability (https://www.exploit-db.com/exploits/46802)

We cat get current web admin password 

![](https://i.imgur.com/OAeNUzO.png)

We transmite local 8843 port to kali

![](https://i.imgur.com/IZb7xso.png)

Connect to https://127.0.0.1:8443/index.html#/settings

![](https://i.imgur.com/aZamv57.png)

Add new task

![](https://i.imgur.com/BJey4bB.png)

Run task 

![](https://i.imgur.com/S451dGP.png)

nc got shell

![](https://i.imgur.com/gMUalJz.png)

Root flag

![](https://i.imgur.com/EMf8pcq.png)

