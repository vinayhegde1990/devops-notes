************
Swap
************

*Some useful links to explain the concepts of Swap*

########
Concepts
########

- https://www.linux.com/news/all-about-linux-swap-space
   
- http://www.linux-tutorial.info/modules.php?name=MContent&pageid=311

- http://aarvik.dk/what-is-swap-memory-and-how-to-use-it/
   
- http://blog.scoutapp.com/articles/2015/04/10/understanding-page-faults-and-memory-swap-in-outs-when-should-you-worry
    



##########
Commands
##########

- **Check total swap space used & sort it descending**

.. code-block:: bash
   :linenos: 
   
   for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -nr | head -10
   for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | awk  '{print $1 " " $2/1024 " MB" }'|sort -k 2 -n -r | head -10
   
- **Alternatively - run below command**

.. code-block:: bash
   :linenos: 
   
   sudo nice top (Press Shift+o → p (To sort processes by swap usage)


################
Configuration
################

- http://www.cyberciti.biz/faq/linux-add-a-swap-file-howto/
   
- http://bencane.com/2016/05/18/creating-a-swap-file-for-tiny-cloud-servers/
   
- https://www.digitalocean.com/community/tutorials/how-to-add-swap-on-centos-7



################################   
Troubleshooting & Log Parsing
################################ 

- http://northernmost.org/blog/find-out-what-is-using-your-swap/
   
- http://www.digitalinternals.com/unix/linux-swap-usage-per-process/379/

- http://www.cyberciti.biz/faq/linux-which-process-is-using-swap/
   
- https://unix.stackexchange.com/questions/294600/i-cant-enable-swap-space-on-centos-7

.. image::  ../source/images/swap-fallocate-centos7.png
    :width: 797px
    :align: center
    :height: 318px
