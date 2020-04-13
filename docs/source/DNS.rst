************
DNS
************

*Some useful links to explain the concepts of DNS*

########
Concepts
########

* Authoritative NS
                * `When a DNS query is made to a server which has the domain's data, it is an authoritative NS, otherwise it will point to other NS or serve cached copies of other NS`
                
* Zone file
                * `simple text file containing the mapping between domain names and IP addresses, e.g : www.google.com`

* Root Servers 
                * `13 servers - a to h, routed to the nearest mirror of the server`

* TLD servers : 
                * `.com [others are : .org, .net, .edu etc]`
                
* Domain Level NS
                * `the server containing the actual records of the requested domain (ns1.google.com, ns2.google.com etc)`

* TTL - Time to live 
                * `A timer. Caching name servers can use this until the TTL runs out`
                
* Records 

.. code-block:: ruby
   :linenos: 

   domain.com.  IN SOA ns1.domain.com. admin.domain.com. (
   12083 ; serial number  - incremented on zone file change, slave NS checks if master NS serial > cached serial & if yes, slave NS requests for updated zone else serves same zone file.
   3h; refresh interval -  Slave NS waits this period to poll the master NS for changes
   30m; retry interval -  Slave NS will retry querying master NS every this period for zone transfer updates
   3w; expiry period -   if slave NS can not contact master for this time, it will no longer return authoritative response for the queried zone
   1h ; negative TTL -  a NS will cache errors for this period
   )
   
Domain Transfer (AXFR)
****************************
- The original DNS specifications `RFC-1034 <http://www.zytrax.com/books/dns/apd/rfc1034.txt>`_ & `RFC-1035 <http://www.zytrax.com/books/dns/apd/rfc1035.txt>`_ envisaged that **slave** (or secondary) DNS servers would poll the **master**. 
- The time between such 'polling' is determined by the refresh value on the domain's `SOA Resource Record <http://www.zytrax.com/books/dns/ch8/soa.html>`_
- The polling process is accomplished by the 'slave' sending a query to the **master** and requesting its current SOA record.
- If serial number of this record is higher than the current one maintained by the **slave** a zone transfer (AXFR) is requested & done on **TCP** Port 53.


DNS uses UDP for DNS queries over port 53
**************************************************************
- DNS uses UDP for to replying to client DNS queries such as client asking DNS server for a Name to IP or IP to NAME resolution.
- The reason is that UDP is not connection oriented, so its light-weight & fast, resulting in faster data transmission of results to client compared to TCP.
- At the same time, if needed then DNS can also work over TCP to serve the DNS queries, but UDP is always preferred because of greater speed.


Why DNS uses TCP for Zone files transfer over port 53
**************************************************************
- DNS uses a **master** & **slave** architecture, in which one main authoritative Name server having all the entries & others are replicated (zone files transferred) from master & also serve DNS queries.
- As there can’t be any inconsistency in Zone files, so to transfer these Zone files DNS uses TCP as the communication protocol, which makes sure that the zone files are transferred reliably.


Resource Records
**********************
* A record
                * map a host to an IP address

``host     IN      A          IPv4_address`` \
``host     IN      AAAA    IPv6_address``

* MX Record
                * map a mail exchange used for the domain

``IN  MX  10  mail.domain.com. (where 10 is record priority. Priority is given to MX with lower values at DNS lookup)``

* PTR 
                * maps an IP address to a reverse name 

How do resolvers work
********************************************
* What happens when you set resolvers in PC (Windows) And / Or Router
                * `A browser 1st checks its internal cache of recent queries which it checks initially otherwise it asks the system resolver for DNS queries (/etc/hosts) else it forwards requests to another resolver.`

.. image::  ../source/images/dns-resolver.png
    :width: 661px
    :align: center
    :height: 582px
    :alt: alternate text


Types of DNS Servers
**************************
- **Recursive:** 
                * `A DNS server which queries other servers until it finds answer to the queried domain. They maintain a cache which is initially checked before sending the app's query to another NS.`

- **Iterative:** 
                * `To be explained`

- **Authoritative-Only :** 
                * `Only answers those queries for which it stores the zones. Does not respond to recursive queries & cache query results.`

- **Caching** : 
                * `It handles recursive queries from clients which handles queries received from the OS stub resolver (/etc/hosts).`
                
                
- https://muchbits.com/soa-dns-records.html

- https://gitlearning.wordpress.com/2015/06/23/dns-server/

- https://danielmiessler.com/study/dns

- https://support.google.com/a/answer/48090?hl=en
   
- http://www.slashroot.in/what-dns-zone-file-complete-tutorial-zone-file-and-its-contents
   
- https://ns1.com/blog/glue-records-and-dedicated-dns
    
- http://www.slashroot.in/mx-record-dns-explained-example-configurations
   
- http://www.slashroot.in/dns-root-servers-most-critical-infrastructure-internet
   
- http://www.slashroot.in/difference-between-iterative-and-recursive-dns-query
   
- http://www.slashroot.in/what-is-dns-cname-record
   
- https://www.digitalocean.com/community/tutorial_series/an-introduction-to-managing-dns
   
- https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts
   
- http://technify.me/systems/dns-explained-so-you-can-understand/
   
- https://luxsci.com/blog/understanding-domain-name-service-dns.html
   
- http://www.menandmice.com/support-training/support-center/knowledgehub/dns-glossary/
   
- http://computer.howstuffworks.com/dns.htm
   
- http://thejimmahknows.com/creating-a-public-dns-server-advertising-an-authoritative-domain/
   
- http://swift.siphos.be/aglara/dnsserver.html
   
- https://geekflare.com/understanding-dns-terminology/

- https://en.wikipedia.org/wiki/Wildcard_DNS_record
        
- DNS Explained via `YouTube <https://www.youtube.com/watch?v=72snZctFFtA>`_


Why are there are only 13-root DNS servers
**********************************************
- https://www.netnod.se/i-root/what-are-root-name-servers

- https://techiemaster.wordpress.com/2016/06/09/why-only-13-root-dns/amp/

- https://miek.nl/2013/November/10/why-13-dns-root-servers/

- https://www.lifewire.com/dns-root-name-servers-3971336


AnyCasting in DNS
**********************
- http://ddiguru.com/blog/45/118
   
- http://ddiguru.com/blog/45/119
    
- http://ddiguru.com/blog/45/120
    
- http://ddiguru.com/blog/45/121


################
Configuration
################

Bind Configuration / Tweaks
*********************************
- https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-ubuntu-14-04
   
- https://www.digitalocean.com/community/tutorials/how-to-configure-bind-as-a-private-network-dns-server-on-centos-7


PowerDNS Configuration / Tweaks
********************************************
- https://www.digitalocean.com/community/tutorials/how-to-install-powerdns-on-centos-6-3-x64
   
- http://www.admin-magazine.com/Articles/Speed-up-Your-Name-Server-with-a-MySQL-Back-End
   
- https://blog.powerdns.com/2015/03/11/introducing-dnsdist-dns-abuse-and-dos-aware-query-distribution-for-optimal-performance/

- https://www.digitalocean.com/community/tutorials/how-to-deploy-and-manage-your-dns-using-dnscontrol-on-ubuntu-18-04


##################################   
Troubleshooting & Log Parsing
##################################   

- http://www.tecmint.com/10-linux-dig-domain-information-groper-commands-to-query-dns/
   
- http://www.cyberciti.biz/faq/linux-unix-dig-command-examples-usage-syntax/
   
- http://www.thegeekstuff.com/2012/02/dig-command-examples/
   
- https://mediatemple.net/community/products/dv/204644130/understanding-the-dig-command
 
- http://anouar.adlani.com/2011/12/useful-dig-command-to-troubleshot-your-domains.html
   
- http://www.cyberciti.biz/faq/dnstop-monitor-bind-dns-server-dns-network-traffic-from-a-shell-prompt/


Check DNS Propagation Issues
************************************************************
- https://intodns.com/
   
- http://www.solvedns.com/
   
- https://www.site24x7.com/dns-lookup.html

- http://viewdns.info/
