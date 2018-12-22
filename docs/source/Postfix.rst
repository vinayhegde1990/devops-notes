***********
Postfix
***********

*Some useful links to cover the basics of Postfix*

########
Concepts
########


################
Configuration
################

- http://blog.schaal-24.de/mail/postscreen-im-kampf-gegen-spam/?lang=en
   
- https://www.howtoforge.com/hardening-postfix-for-ispconfig-3
   
- https://workaround.org/ispmail/squeeze/postfix-domain-types
   
- https://workaround.org/article/postfix-database-configuration
   
- https://www.howtoforge.com/virtual_postfix_antispam
   
- https://rtcamp.com/tutorials/mail/
   
- https://www.linode.com/docs/email
   
- https://www.linode.com/docs/email/running-a-mail-server

SSL/TLS on Postfix
*********************
- https://blog.kruyt.org/postfix-and-tls-encryption/
   

################################   
Troubleshooting & Log Parsing
################################

Queue Management
***************************
- http://www.postfix.org/QSHAPE_README.html
   
- https://easyengine.io/tutorials/mail/postfix-queue/
   
- http://wiki.zimbra.com/wiki/Managing_The_Postfix_Queues
   
- http://www.tullyrankin.com/managing-the-postfix-queue
   
- https://www.wirehive.net/blog/2014/11/07/5-top-tips-for-reviewing-your-postfix-mail-queue
   

##########
Commands
##########
   
- **Sorting queued mails by From address**

.. code-block:: bash
   :linenos: 
   
   sudo mailq | awk '/^[0-9,A-F]/ {print $7}' | sort | uniq -c | sort -n
   
- **Holding queued mails by From address**

.. code-block:: bash
   :linenos: 
   
   sudo mailq| grep '^[A-Z0-9]'| grep <sender-ID>| cut -f1 -d' ' | tr -d \*|sudo postsuper -h -
   
- **Holding queued mails by To address**

.. code-block:: bash
   :linenos: 
   
   sudo mailq | tail -n +2 | grep -v '^ *(' | awk  'BEGIN { RS = "" } { if ($8 == "<recipient>") print $1 } ' | tr -d '*!' | sudo postsuper -h -

- **Holding queued mails by Domain**

.. code-block:: bash
   :linenos: 
   
   sudo mailq| grep '^[A-Z0-9]'| grep @<domain>| cut -f1 -d' ' | tr -d \*|sudo postsuper -h -

- **Holding emails from the [active|deferred] queue based on subject**

.. code-block:: bash
   :linenos: 
   
   sudo find /var/spool/postfix/[active|deferred]/ -type f  -exec grep -il '<subject>' '{}' \; | xargs -n1 basename | sudo postsuper -h -
   
- **Removing Mails based on sender Address**

.. code-block:: bash
   :linenos: 
   
   sudo mailq| grep '^[A-Z0-9]'| grep <sender-ID>| cut -f1 -d' ' | tr -d \*|sudo postsuper -d -

- **Removing Mails based on Domain**

.. code-block:: bash
   :linenos: 
   
   sudo mailq| grep '^[A-Z0-9]'| grep @<domain>| cut -f1 -d' ' | tr -d \*|sudo postsuper -d -

- **Delete mails to a specific mail address**

.. code-block:: bash
   :linenos: 
   
   sudo mailq | tail -n +2 | grep -v '^ *(' | awk  'BEGIN { RS = "" } { if ($8 == "<recipient-ID>") print $1 } ' | tr -d '*!' | sudo postsuper -h -
