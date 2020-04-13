************
SSL
************

*Some useful links to explain the concepts of SSL*

########
Concepts
########

- https://tls.ulfheim.net

- https://www.digitalocean.com/community/tutorials/a-comparison-of-let-s-encrypt-commercial-and-private-certificate-authorities-and-self-signed-ssl-certificates

- https://scotthelme.co.uk/https-cheat-sheet/
   
- https://www.digicert.com/ssl.htm

.. image::  ../source/images/web-servers-ssl-handshake.png
    :width: 1098px
    :align: center
    :height: 672px
   
- http://grahamc.com/blog/openssl-madness-how-to-create-keys-certificate-signing-requests-authorities-and-pem-files/
   
- https://www.digicert.com/csr-creation.htm
   
- http://swift.siphos.be/aglara/certificates.html
   
- https://www.openssl.org/docs/manmaster/apps/verify.html
   
- http://www.openssl.org/docs/manmaster/apps/x509.html
   
- http://www.slashroot.in/understanding-working-secure-socket-layerssl
   
- http://www.slashroot.in/understanding-ssl-handshake-protocol


FAQs on SSL
#############
- https://timnash.co.uk/guessing-ssl-questions/
   
- http://www.martfox.com/customer/knowledgebase/140/Why-a-SSL-Requires-Dedicated-IP.html

- https://dzone.com/articles/introduction-to-ssl-for-managers
   
- https://www.nutsandboltsmedia.com/does-your-website-really-need-ssl/

- https://www.slashroot.in/how-does-ssltls-chain-certificates-and-its-validation-work

- https://blog-cloudflare-com.cdn.ampproject.org/c/s/blog.cloudflare.com/rfc-8446-aka-tls-1-3/amp/

- https://serverfault.com/questions/9708/what-is-a-pem-file-and-how-does-it-differ-from-other-openssl-generated-key-file

- https://www.troyhunt.com/life-is-about-to-get-harder-for-websites-without-https/

- https://www.troyhunt.com/on-the-perceived-value-ev-certs-cas-phishing-lets-encrypt/

- https://www.troyhunt.com/extended-validation-certificates-are-dead/


Server Name Indication
###########################
- https://devcentral.f5.com/articles/ssl-profiles-part-7-server-name-indication
   
- http://wiki.apache.org/httpd/NameBasedSSLVHostsWithSNI
   
- https://www.digicert.com/ssl-support/apache-multiple-ssl-certificates-using-sni.htm
 

################
Configuration
################

Basics of OpenSSL Commands for CSR, Keys & Certs
#######################################################
- https://www.digitalocean.com/community/tutorials/openssl-essentials-working-with-ssl-certificates-private-keys-and-csrs
   
Wildcard SSL on sub-domain
##############################
- http://stackoverflow.com/questions/2115611/wildcard-ssl-on-sub-subdomain
   
- http://serverfault.com/questions/566426/does-each-subdomain-need-its-own-ssl-certificate
   
- http://serverfault.com/questions/104160/wildcard-ssl-certificate-for-second-level-subdomain


Switching from HTTP to HTTPs
##############################
- https://www.smashingmagazine.com/2017/06/guide-switching-http-https/
   
- http://searchengineland.com/http-https-seos-guide-securing-website-246940
   
- https://yoast.com/moving-your-website-to-https-ssl-tips-tricks/


Creating SAN SSL certificate
##############################
- https://geekflare.com/san-ssl-certificate/


#########################
Tuning & Hardening
#########################
- http://heartbleed.com/
   
- http://www.troyhunt.com/2014/04/everything-you-need-to-know-about.html
 
- https://www.yahoo.com/tech/heres-what-you-need-to-know-about-the-heartbleed-bug-82120054478.html
   
- http://thehackernews.com/2014/04/heartbleed-bug-explained-10-most.html
   
- http://kb.odin.com/en/118918
   
- https://security.stackexchange.com/questions/8210/what-vulnerabilities-could-be-caused-by-a-wildcard-ssl-cert

- http://www.jamescoyle.net/how-to/1073-bash-script-to-create-an-ssl-certificate-key-and-request-csr
   
- https://rtcamp.com/wordpress-nginx/tutorials/ssl/multidomain-ssl-subject-alternative-names/
   

Hardening Your Web Server’s SSL Ciphers
#############################################
- https://hynek.me/articles/hardening-your-web-servers-ssl-ciphers/

- https://cipherli.st/
   
- https://mozilla.github.io/server-side-tls/ssl-config-generator/
 

##############################
Troubleshooting & Log Parsing
##############################
- https://www.sslshopper.com/ssl-certificate-tools.html
   
- https://cheapsslsecurity.com/ssltools/
   
- http://geekflare.com/ssl-test-certificate/
   
- https://serversforhackers.com/self-signed-ssl-certificates
   
#############
Commands
#############
- https://www.sslshopper.com/article-most-common-openssl-commands.html
   
- http://www.shellhacks.com/en/HowTo-Check-SSL-Certificate-Expiration-Date-from-the-Linux-Shell
   
- https://cryptoreport.websecurity.symantec.com/checker/
   
- https://www.digicert.com/help/
   
   
Free SSL Certificates : LetsEncrypt
###################################
- https://www.digitalocean.com/community/tutorials/an-introduction-to-let-s-encrypt

- https://geekflare.com/free-ssl-tls-certificate/
   
- https://serversforhackers.com/video/letsencrypt-for-free-easy-ssl-certificates
   
- https://letsencrypt.org/
   
- https://digitz.org/blog/lets-encrypt-ssl-centos-7-setup/
   
- https://certbot.eff.org/lets-encrypt/centosrhel7-nginx.html
