************
Graphing
************

*Some useful links to explain the concepts of Graphing*

########
Concepts
########

**Cacti**

- http://www.cacti.net/index.php


**Metrics**

- http://blog.4aiur.net/2012/01/installing-and-configuring-graphite-on-centos/
  
- http://kaivanov.blogspot.in/2014/07/metrics-visualisation-and-collection.html


###########
Ganglia
###########

- http://www.slashroot.in/introduction-ganglia-monitoring-and-graphing-tool

- https://www.digitalocean.com/community/tutorials/introduction-to-ganglia-on-ubuntu-14-04
   
- https://sachinsharm.wordpress.com/2013/08/17/setup-and-configure-ganglia-3-6-on-centosrhel-6-3/


What Ganglia does
#####################
   
        * `Graph different properties of a server such as CPU,memory,load,etc`

        * `Compare the graphing trend of those properties with previous trend & identify which node or host is causing the issue easily from the trend.`

        * `Make custom metrics for graphing for different process.`

        * `Machines from different data centers which are part of one single cluster must be represented in that single cluster in a single interface.`
 

Important points
#################

        * **Node** : `SINGLE machine sending data to Ganglia monitoring daemon. (All individual servers are nodes, can or can't be part of a cluster)`

        * **Cluster** : `All nodes that are used for any particular purpose is a CLUSTER.`

        * **Grid** : `Collection of clusters is a GRID.`


Parts of Ganglia Monitoring Tool
##################################
* **1. Gmond :**

        * `Ganglia Monitoring daemon (Service that needs to be installed on each & every node that needs to be monitored)`

        * `Sends data via XML over TCP & main configuration file` : ``/etc/gmond.conf``

* **2. Gmetad :**

        * `Collects data from Gmond daemons & stores in RRD (Round robin database)`

        * `Main configuration file is /etc/gmetad.conf & should be installed on one node of each cluster`

* **3. RRD tool :**

        * `Used by Ganglia to store data for visualization (graphing) & store data of particular time intervals & then graphs the same.`

* **4. PHP Front-End :**

        * `A web interface on the master node that displays graphs and metrics from data in the RRD tool.`


################
Configuration
################

- http://linuxdrops.com/install-ganglia-monitoring-system-on-centos-rhel/
   
- https://sachinsharm.wordpress.com/2013/08/17/setup-and-configure-ganglia-3-6-on-centosrhel-6-3/
   
- https://sachinsharm.wordpress.com/2013/08/19/setup-and-configure-ganglia-python-modules-on-centosrhel-6-3/

- http://a4amittripathi.blogspot.in/2014/01/how-to-configure-and-install-ganglia-in.html
   
- http://www.ibm.com/developerworks/library/l-ganglia-nagios-1/


################################   
Troubleshooting & Log Parsing
################################

- https://ahmadchaudary.wordpress.com/tag/ganglia-monitoring/
   
- http://rowsandcolumns.blogspot.in/2010/07/compiling-ganglia-errors-and-problems.html
