# LE4ISPC (Single or Multi Server Setup)
LE4ISPC is an ancronym for Let's Encrypt for ISPConfig, specifically version 3.1, with auto updater for ispserver.pem, whether single or multi server setup, and for other services like Postfix+Dovecot, Pure-ftpd, Monit etc. It will automatically create Let's Encrypt for any ISPConfig server hostname FQDN if none exists; and secure its control panel and other services; if they are available and installed. The script is meant for Debian, Ubuntu and other similar derivatives as the server OS.

# STATUS
Obsolete and abandoned since the release of ISPConfig 3.2. It will never be updated. ISPConfig user should rely on default Let's Encrypt client hook in ISPConfig installer or updater in creating and recreating ispserver .crt .key and .pem and restarting all related services, rather than rely on incron, since hook only runs at renewal but incron will definitely use server resources to constantly monitor the ISPConfig server LE SSL Certs renewal and as such might also fail sometimes. Hook will have higher chances of working too since it will only run if the renewal is successful. 

# HOW TO REMOVE LE4ISPC
In your terminal, in root mode, simply run this after you have installed any of your ISPConfig server build:
```
cd /tmp
wget https://raw.githubusercontent.com/ahrasis/LE4ISPC/master/le4ispc-remover.sh
chmod +x le4ispc-remover.sh
./le4ispc-remover.sh
```
Note: You can add "--no-check-certificate" at the end of wget line if it is an issue to you.

# OLDER HOW-TO'S
https://github.com/ahrasis/LE4ISPC/tree/master/old/le4ispc

https://github.com/ahrasis/LE4ISPC/tree/master/old/nginx

https://github.com/ahrasis/LE4ISPC/tree/master/old/apache

# LICENSE
BSD3
