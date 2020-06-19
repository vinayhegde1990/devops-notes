**********
MySQL
**********

*Some useful links to explain the concepts of MySQl*


########
Concepts
########
- http://etutorials.org/SQL/MySQL/
   
- https://serversforhackers.com/series/mysql
   
- http://www.rathishkumar.in/2016/04/understanding-mysql-architecture.html?

Difference between MyISAM and InnoDB Storage engines
******************************************************************
- http://blog.danyll.com/myisam-vs-innodb/
   
- http://www.rapidprogramming.com/questions-answers/differences-between-innodb-and-myisam-in-mysql-innodb-vs-myisam-1533
 

##########
Commands
##########
- http://www.mysqltutorial.org/
 
 
################
Configuration
################

- https://www.percona.com/blog/2014/11/12/log-rotate-and-the-deleted-mysql-log-file-mystery/
   
- http://blog.oneiroi.co.uk/mysql/mysql-slow-query-log-rotation/
   
- http://mysql.az/2015/05/12/mysql-logrotate-script/
     
- https://www.question-defense.com/2009/12/20/configure-logrotate-to-rotate-and-flush-mysql-logs-without-a-password
   
- http://etutorials.org/SQL/MySQL/Part+III+MySQL+Administration/Chapter+11.+General+MySQL+Administration/Maintaining+Log+Files/
   
- https://opensourcedbms.com/dbms/how-to-upgrade-mysql-5-5-to-mysql-5-6-on-centos-6-3-red-hat-fedora/
   
Backing Up | Restore Databases via Command Line
******************************************************************
- https://in.godaddy.com/help/backup-mysql-databases-on-your-server-linux-17547
   
- http://www.mysqltutorial.org/how-to-backup-database-using-mysqldump.aspx
   
- https://www.liquidweb.com/kb/how-to-back-up-mysql-databases-from-the-command-line/
   
- https://www.tecmint.com/mysql-backup-and-restore-commands-for-database-administration/


Configuring MariaDB for remote access
*********************************************
- https://mariadb.com/kb/en/library/configuring-mariadb-for-remote-client-access/

Removing a MySQL user with his privileges 
***********************************************
- https://nsaunders.wordpress.com/2007/04/30/removing-a-mysql-user/
   
- https://www.a2hosting.in/kb/developer-corner/mysql/managing-mysql-databases-and-users-from-the-command-line


Information on MySQL Bin logs
************************************
- http://www.cyberciti.biz/faq/what-is-mysql-binary-log/
     

Replication (Master-Master)
********************************
- https://www.digitalocean.com/community/tutorials/how-to-set-up-mysql-master-master-replication


Replication (Master-Slave)
********************************
- http://www.tecmint.com/how-to-setup-mysql-master-slave-replication-in-rhel-centos-fedora/
		  
- https://www.rackspace.com/knowledge_center/article/mysql-master-slave-replication
   
- https://www.digitalocean.com/community/tutorials/how-to-set-up-master-slave-replication-in-mysql
   
- http://sharadchhetri.com/2013/11/21/setup-mysql-master-slave-replication-in-centos-6/
   
- http://aarvik.dk/how-to-set-up-master-slave-replication-in-mysql/

- http://plusbryan.com/mysql-replication-without-downtime

- https://blog.marceloaltmann.com/en-how-does-mysql-replication-works-pt-como-funciona-a-replicacao-no-mysq/


Reset forgotten MySQL password
************************************
- https://www.digitalocean.com/community/tutorials/how-to-reset-your-mysql-or-mariadb-root-password
   
- http://www.cyberciti.biz/faq/mysql-change-root-password/
   
- https://www.liquidweb.com/kb/change-a-password-for-mysql-on-linux-via-command-line/
   
- https://www.codeenigma.com/community/blog/restoring-mysql-root-user


##################
Tuning & Hardening
##################
- http://blog.webyog.com/2012/11/20/how-to-monitor-mysql-replication/
   
- https://www.digitalocean.com/community/tutorials/how-to-secure-mysql-and-mariadb-databases-in-a-linux-vps
 
- https://www.percona.com/blog/2013/04/18/rotating-mysql-slow-logs-safely/ 
   
- http://www.pontikis.net/blog/how-and-when-to-enable-mysql-logs
   
- https://serversforhackers.com/c/mysql-network-security
   
- http://www.proxysql.com

- https://severalnines.com/resources/database-management-tutorials/mysql-load-balancing-haproxy-tutorial


To change the value of expire_log_days without MySQL restart
******************************************************************
- https://www.sebastien-han.fr/blog/2013/02/15/purge-mysql-binary-logs/
   
To enable various logs via my.cnf or on the fly without restart
******************************************************************
- http://www.pontikis.net/blog/how-and-when-to-enable-mysql-logs

Perl script to analyses system MySQL variables & optimize accordingly
*************************************************************************
- https://major.io/mysqltuner/
   
Tool to convert xls files into SQL
***********************************
- https://sqlizer.io/



################
Troubleshooting
################

- https://alvinalexander.com/blog/post/mysql/how-show-open-database-connections-mysql

- https://www.tecmint.com/mysqladmin-commands-for-database-administration-in-linux/

- http://www.plugged.in/databases/mysql-server-wont-start-pid-file-errors.html
   
- https://major.io/2008/06/24/mysql-error-1040-too-many-connections/
   
- https://www.digitalocean.com/community/tutorials/how-to-use-mytop-to-monitor-mysql-performance

Checking for replication Lags
************************************
- https://www.percona.com/blog/2007/10/12/managing-slave-lag-with-mysql-replication/   

- https://www.percona.com/blog/2014/05/02/how-to-identify-and-cure-mysql-replication-slave-lag/

Various MySQL error codes
*******************************
- http://www.fromdual.com/mysql-error-codes-and-messages
   
- https://major.io/2007/08/09/mysql-error-codes/


Fix for the ERROR 1396
***************************
- https://stackoverflow.com/questions/5555328/error-1396-hy000-operation-create-user-failed-for-jacklocalhost

.. image::  ../source/images/mysql-error-1396.png
    :width: 769px
    :align: center
    :height: 291px
    :alt: alternate text
