************
Hardware
************

*Some useful links to explain the concepts of Hardware (Dell / SuperMicro)*

- http://www.thegeekstuff.com/2008/11/how-to-get-hardware-information-on-linux-using-dmidecode-command/
   
- http://www.tecmint.com/how-to-get-hardware-information-with-dmidecode-command-on-linux/
   
- http://linoxide.com/linux-command/how-to-display-system-hardware-information-in-bios/
   
- http://www.thegeekstuff.com/2014/04/lspci-examples
   
- https://linuxconfig.org/getting-know-a-hardware-on-your-linux-box
   
- https://blog.mattbrock.co.uk/monitoring-perc-raid-controllers-and-storage-arrays-on-dell-poweredge-servers-with-debian-and-ubuntu/


############
Dell OMSA
############

Concepts
*************
- http://cavepopo.hd.free.fr/wordpress/linux/dell-server-utility-omreport/
     
- http://public.support.unisys.com/pcproducts/esx/docs/delldocs5.4/en/dosa/storageug/cli.html
   
- https://stuff.mit.edu/afs/athena/dept/cron/documentation/OldFiles/Manuals/dell-server-admin/en/Dosa/CLI/storage.htm
   
- https://discuss.zendesk.com/hc/en-us/articles/201831218-Useful-omreport-commands-for-DCA-V1
   
- https://cs.uwaterloo.ca/~brecht/servers/docs/PowerEdge-2600/en/Dosa/CLI/cli_cc5s.htm


Commands
*************
- **We use 2 commands to monitor / change parameters in Dell servers**

.. code-block:: bash
   :linenos:

   omreport - Checks the server details via specified parameters.

   omconfig - Modifies the server details via specified parameters.
                        

Examples : 
****************

- **Will list all possibly available system / chassis / storage domain commands**

.. code-block:: bash
   :linenos:

   sudo omreport system -?  | omreport chassis -?  | omreport storage -?

- **Retrieve general system information**

.. code-block:: bash
   :linenos:

   sudo omreport system summary | less

- **Display the Hardware logs**

.. code-block:: bash
   :linenos:
  
   sudo omreport system esmlog

- **Retrieve the RAID configuration**

.. code-block:: bash
   :linenos:
   
   sudo omreport storage vdisk controller=0

- **Clearing the logs**

.. code-block:: bash
   :linenos:
   
   sudo omconfig system esmlog action=clear (Replace esmlog with alertlog or cmdlog, esmlog is the hardware log)


################
Configuration
################

- http://cavepopo.hd.free.fr/wordpress/linux/how-to-create-a-raid-array-using-omconfig-omreport-cli/
   
- http://cavepopo.hd.free.fr/wordpress/linux/how-to-expand-a-raid-array-using-omconfig-omreport-cli/



########
IPMITool
########

- https://discuss.zendesk.com/hc/en-us/articles/206396927-How-to-work-on-IPMI-and-IPMITOOL


########
MegaCLI
########

- https://artipc10.vub.ac.be/wordpress/2011/09/12/megacli-useful-commands/

- https://things.maths.cam.ac.uk/computing/docs/public/megacli_raid_lsi.html
