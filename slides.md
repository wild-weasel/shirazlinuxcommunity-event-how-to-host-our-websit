---
theme: seriph
colorSchema: auto
layout: image
image: ./public/3.jpg
#canvasWidth: 900
---

---
layout: center
class: text-center

---

<br><br/>

# **Introducing Myself**

<br><br/>

## *Hossein Esmaeilnejad*

### Network and System Administrator

<br><br/>

#### T.me/HosseinESMN

<br><br/><br><br/><br><br/><br><br/>

---
layout: cover
background: ./public/methods.jpg

---

## ***Tips on Making Good Choices:***
<br><br/><br><br/><br><br/><br><br/>
<br><br/><br><br/><br><br/><br><br/>
<br><br/><br><br/><br><br/><br><br/>
<br><br/><br><br/><br><br/><br><br/>

---
layout: left

---

# *Shared-Host* 

#### **physical server share resources with one or more other hosts and controling with control panel**
 - **minimum cost & technical knowledge**
 - **create backup automatic & simple**
 - **minimum admin overhead**
 - **protect hosts with firewall control panel & logging and monitoring systems**
 - **not scalabel  (fixed resource ) and medium performance**
 - **minimum control over your host**

---
layout: image
image: ./public/zpanel.png

---
---
layout: image
image: ./public/virtualmin.png

---
---
layout: image
image: ./public/ispconfig.png

---
---
layout: image
image: ./public/froxlor.png

---
---
layout: image
image: ./public/Cloud panel.png

---
---
layout: left

---

# *Virtual Dedicated & Private Server (VDS/VPS):*
### **website will host on VPS/VDS that provided by virtualization hypervisor**
### **(KVM-ESXI-proxmox) which this hypervisor installed on ber-metal servers**

 - **provider may set hypervisor somehow that users and vps use shared resources in server (disks,bandwidth)**
 - **Scalability resource as your plan is grows but still limited by provider**
 - **more control & Customization on VPS/VDS  by full root access (deploy-install your own control panel management,monitoring and service)**
 - **security & Reliability by isolated from other vps-vds while on the same server and protect with layers of firewalls by provider**
 - **user need to know technical knowledge**
 - **admin overhead for services maintenance**
 - **cost is more than shared-host but cost-effective than dedicated servers**

---
layout: left

---
# *Dedicated Host (DS):*

#### **user leases an entire server from provider and not shared with anyone else**
 - **More flexible than shared-hosting, as user have full control over the server**
 - **huge cost & maintenance**
 - **it is secure and reliable as you have full access**


---
layout: left

---

# *Cloud Hosting:*
### **website will host on multi servers or VPS/VDS that located in data centers**
**porvide several service for users to host website such as a:**
 ##### **Infrastructure-as-a-Service (IaaS) :**
 ###### **so user no need to maintain and manage servers hardware**
 ##### **Platform-as-a-Service (PaaS):**
 ###### **so user no need to install operating systems, virtualization virtual machines,docker [containers]**
 ##### **software-as-a-Service (SaaS):**
 ###### **so user no need to install applications**
 - **Reliability and performance**
 - **pay as you go cost**
 - **quickly scalabel,flexible**
 - **Reliability by interconnected networks redundant power and cooling systems, multiple internet connections,to ensure maximum uptime to make more accessable website in anytime at anywhere**
 - **Security (DDOS protection,SSL/TLS,Fierwalls,advance authenticate)**


---
layout: image
image: ./public/cloud.png

---
---  
layout: image
image: ./public/sh-vpds-ds-C.jpg

---
---
layout: left
class: text-left

---

# **Minimum Requirements for up or website:**
(Self-Hosting)

<br><br/>

* ### *Webserver*
   ###### **Nginx, Apache, OpenLiteSpeed, caddy**
* ### *Domain*
  ###### **Registration TLD**
* ### *DNS* 
  ###### **A Record, CNAME Record**
* ### *SSL Certificate*
  ###### **Free (self-signed,trusted certificate authority (CA)) or Paid**
* ### *CDN*
  ###### **Cloudfleare, Gcore**

---
layout: center
class: text-center

---

### ***Caddy vs. Apache2 vs. Nginx***

![Local Image](caddy-nginx-apache.png)

---
layout: center
class: text-center

---

# Example of NginX Configuration

```nginx
server {
    listen                  443 ssl;
    server_name             www.example.com;
    ssl_certificate         /etc/letsencrypt/live/example.com/fullchain.pem;
    ssl_certificate_key     /etc/letsencrypt/live/example.com/privkey.pem;
    location / {
        index index.html;
        root /var/www/html;
    }
}
```
---
layout: center

---

# Example of Caddy Configuration

```nginx
example.com {
    encode gzip

    handle /api/* {
        reverse_proxy backend:8000
    }

    handle {
        root * /path/to/site
        try_files {path} /index.html
        file_server
    }
}
```

---
layout: center

---

# Example of Apache2 Configuration

```xml
<VirtualHost *:80>
       ServerName mywebsite.com
       DocumentRoot /var/www/mywebsite
       ErrorLog ${APACHE_LOG_DIR}/error.log
       CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

---
layout: image-right
image: ./public/url5.png
#586*655
class: text-left
---
## *Domain Fundamental*
### *what is :*  
- #### *Domain-name Registry ?*
   ##### OU that manage TLD .com .net -- that specifically by maintaining the records of which individual domains-names belong to who
   ##### These registries are managed by (IANA),(ICANN) that coordinates several processes and databases that support the Internet’s basic functionality.

- #### *Domain-name Registrar ?*
   ##### business that handles reservation of domain names to IP and sels TLD to registrant
   ##### the registrar must notify VeriSign and paye fee — to registry for TLD domains that lease to end users (registrant)

-  #### *Domain-name Registration | TLD ?*
   ##### process that user reserving name to Ip address.
   ###### **come at the end of domain-names right after root, and play important role for classifying domain-names,DNS-lookups and resolve in TLD servers**

---
layout: image-right
image: ./public/url4.jpg
#586*655
class: text-left

---

- #### *Fully qualified domain name(FQDN) ?*
  ##### referred to as an absolute domain name contain third-level+second-level+top-level domain that sepreat by (dot)
   ##### The topmost layer of every domain name is the DNS root zone
- #### *Sub-Domain ?*
  ##### Domain-Name that is under the main domain In the Domain Name System (DNS) hierarchy

- #### *Domain-Name ?*
   ##### name that reffering to website that pointed to  ip address and easy to remmember it
   ##### (Thanks to the DNS system records)

- #### Uniform Resource Locator (URL)
   ##### (URL) contain all this structures + query string and parameters that start with ? mark that incloude KEY-VALUE 

---
layout: image-right
image: ./public/dns2.png
#586*655
class: text-left

---

### ***Why DNS Records is important ?***
 ##### The DNS records is instructions that live on DNS servers 
 ##### These instructions are vital to DNS lookup and reverse DNS lookups.
 - ###### DNS A record points the IP address to a given domain name. 
 - ###### CNAME record points sub-domain to a given domain name as a aliase.

 ```
 www.example.com 3600 CNAME example.com
 example.com     3600   A    192.1.2.3
 ```
 ##### Note:
 - ###### do not forget to configure your apache/nginx to accept connections for both domain names (redirection).
 - ###### From the point of view of DNS it is a totally normal subdomain

---
layout: image
image: ./public/DNS_schema.svg.png

---
---
layout: image-right
image: ./public/ssl.png
#586*655
class: text-left

---

## ***What is SSL/TLS ?***
###### is an encryption-based Internet security protocol that provides privacy, authentication, and integrity

#### ***Why Important to using That?***
##### necessary for:
- ###### stablishing encrypted connection between user's browser and the web server using HTTPS protocol
- ###### encrypts data that is transmitted across the web
- ###### prevent on-path attacks, domain spoofing so attacker can not intercept this data

 
<br><br/>
---
layout: image-right
image: ./public/how-ssl.jpg

---
## ***how dose ssl/tls work ?***
   #### **A TLS handshake uses asymmetric encryption by two keys:**
   #### public key: which the server makes available publicly
   #### private key: which is kept secret and only used on the server side.
   #### Data encrypted with the public key can only be decrypted with the private key.

---
layout: image-right
image: ./public/error-page.jpg

---

### ***What is SSL/TLS Certificate ?***
#### ***Type of SSL/TLS Certificate :***
##### Certificate Authorities (CA) is an outside party who can confirm that the website owner is who they say they are.
##### They keep a copy of the certificates they issue. and are responsible for issuing SSL certificates by using public-key of orginal web-sites  incloude :
 ##### - Domain Validation
 ##### - Organization Validation
 ##### - Extended Validation
###### CA validate certificat by digital-signature
###### Website owners need to obtain an SSL certificate from a certificate authority, and then install it on their web server
###### browsers know about CA so that's browsers job that confirm  this certificate is validate or not if not you will see this error page 

---
layout: image-right
image: ./public/letsencrypt.jpg

---
 - ### ***Trusted CA***:
 #### - Let's Encrypt by certbot and ssl for free
 ```
  https://certbot.eff.org/
 ```

 ```
  https://www.sslforfree.com/
 ```

---
layout: image-right
image: ./public/ssl2.png

---

##### - **Single-Domain SSL certificat**
  ###### applies to only one domain-name
##### - **Wildcard SSL certificat**
  ###### applies to only one domain-name. it also includes that domain's subdomains.
##### - **Multi-Domain SSL certificat**
  ###### apply to multiple unrelated domain-names.

---
layout: left

---
 - ### ***Self-Signed:***
 ###### website owner can create their own SSL certificate, (self-signed certificates).
 ###### However, browsers do not consider self-signed certificates as trusted like CA.

 ```
 sudo openssl req -x509 -nodes -days 365 -newkey\
 rsa:2048 -keyout\
 /etc/ssl/private/nginx-selfsigned.key -out\
 /etc/ssl/certs/nginx-selfsigned.crt

 ```

---
layout: text-left

---

 #### -1.install openssl and cheack out version info:

 ```
 sudo apt-get install openssl
 openssl version -a

 ```
 #### -2.make directory in webserver for ssl

 ```
 cd  /etc/nginx && mkdir ssl
 ```
 #### -3.generate private-key
 ```
  openssl genrsa 2048 > site-name.pem or .key

 ```
 #### -4.request a certificate for FQDN domain
 ```
  openssl req -new -key site-name.pem > site-name.csr

 ```
 #### -5.sign the certificate 
 ```
 openssl x509 -in site-name.csr -out site-name.crt -req site-name.pem days 365

 openssl x509 -text -noout -in site-name.crt

 ```
 #### -6.edit webserver ssl config files (nginx)

 ```
 server {
      ssl_certificate /etc/ssl/certs/sitename.crt;
      ssl_certificate_key /etc/ssl/private/site-name.pem or .key;
      }
 ```
---
layout: text-left

---
 #### -7.check webserver config

 ```
 nginx -t

 ```
 #### -8.restart web server (nginx)

 ```
   service nginx restart

 ```
 #### -9.redirect http traffic to https:

 ```
 server {
   listen 80 default_server;
   server_name _;
   return 301 https://$host$request_uri;
   }
 ```

---
layout: image
image: ./public/cdn.png

---
<br><br/>

# **What is a content delivery network (CDN)?**

## ***Why use CDN?***

## ***How dose CDNs work?***

---
layout: image

---

# **let's up our website**

## **Docker+Nginx+CDN**
##### **https://event10.shirazlinuxcommunity.ir**
---
layout: image
image: ./public/exampelyaml.jpg

---

