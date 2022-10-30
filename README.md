# Host-A-Website-on-Windows-10
Document how to host a website on a Windows 10 machine 

## Install XAMPP
1. Go to https://www.apachefriends.org/
2. Download the version that suit your operating system (in this case is Windows)
3. Install XAMPP follow the prompts

(this XAMPP uses Apache HTTP Server as the backend to host your website. There are a few other backend server application like NGINX, Microsoft Internet Information Services (IIS), Lighttpd and Sun Java System Web Server)

## Upload your website to xampp folder
the default path for website file is "C:/xampp/htdocs"

## Get SSL Certificate

## Get domain name and link domain name to your public IP address

## Port Forwarding

## Configuration file change to enable ssl certificate
1. Find "httpd-ssl.conf" file
Two ways of finding the file: 1. within XAMPP Control Panel -> click the "Config" button on Apache row -> click the second file on the drop-down 2. Default path for config file is "C:/xampp/apache/conf/extra"
2. Open the "httpd-ssl.conf" file and make the following edits
<VirtualHost _default_:443>
**DocumentRoot "C:/xampp/htdocs/your_website"**
**ServerName www.your_domain_name.domain:443**
**ServerAdmin admin@your_domain_name.domain**
ErrorLog "C:/xampp/apache/logs/error.log"
TransferLog "C:/xampp/apache/logs/access.log"

SSLEngine on
**SSLCertificateFile "C:/xampp/apache/ssl/xxxxxxx_www.your_domain_name.domain_public.crt"**
**SSLCertificateKeyFile "C:/xampp/apache/ssl/xxxxxxx_www.your_domain_name.domain.key"**
**SSLCertificateChainFile "C:/xampp/apache/ssl/xxxxxxx_www.your_domain_name.domain_chain.crt"**


## How to set a static IP address

1. Go to Control Panel -> Network and Internet -> Network and Sharing Center ->Change adapter settings
2. Select the adapter you are currently using (e.g. Ethernet or Wi-Fi) -> right click ->Properties
3. Double click on Internet Protocol Version 4 (TCP/IPv4)
4. Select Use the following IP address:
IP address: 192.168.0.14

Subnet mask: 255.255.255.0

Default gateway: 192.168.0.1

(some of the information above can be obtained from Status or ipconfig command)






