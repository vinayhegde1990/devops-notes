************
Utilities
************

################################
Environment Variables {ENV}
################################

*Some useful links to explain the concepts of Environment Variables*

- https://www.guru99.com/linux-environment-variables.html

- https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps

- https://www.slashroot.in/difference-between-bashrc-and-bashprofile

- https://www.cyberciti.biz/faq/linux-list-all-environment-variables-env-command/


################
Schedulers
################

*Some useful links to cover the working of Crontab and Systemd Timers*

Cron Tab
*************

- https://www.thegeekstuff.com/2009/06/15-practical-crontab-examples/

- https://www.cyberciti.biz/faq/linux-show-what-cron-jobs-are-setup/

- https://www.pantz.org/software/cron/croninfo.html

.. image::  ../source/images/utilities-cron-syntax-1.png
    :width: 846px
    :align: center
    :height: 183px
        

.. image::  ../source/images/utilities-cron-syntax-2.png
    :width: 1180px
    :align: center
    :height: 1953px


Systemd Timers
*********************

- https://opensource.com/article/20/7/systemd-timers

- https://www.neteye-blog.com/2022/12/start-using-systemd-timers-instead-of-cron-anacron/

- https://dev.to/bowmanjd/schedule-jobs-with-systemd-timers-a-cron-alternative-15l8

- https://unix.stackexchange.com/questions/278564/cron-vs-systemd-timers

- https://www.reddit.com/r/linuxadmin/comments/k8l272/systemdtimers_vs_cron/

- https://akashrajpurohit.com/blog/systemd-timers-vs-cron-jobs/

   
Online Utilities to generate crons
***********************************
   
- https://crontab-generator.org/


########
GREP
########

*Some useful links to cover the working of Grep*

- https://thevaluable.dev/grep-cli-guide-examples/

- https://www.linode.com/docs/guides/how-to-use-grep-command/
   
- https://www.cyberciti.biz/faq/searching-multiple-words-string-using-grep/
   
- https://www.thegeekstuff.com/2011/10/grep-or-and-not-operators/
   
- https://www.digitalocean.com/community/tutorials/using-grep-regular-expressions-to-search-for-text-patterns-in-linux

- https://alvinalexander.com/unix/edu/examples/grep.shtml

- https://stackoverflow.com/questions/2427913/how-can-i-grep-for-a-string-that-begins-with-a-dash-hyphen

- https://stackoverflow.com/questions/221921/use-grep-exclude-include-syntax-to-not-grep-through-certain-files

- https://stackoverflow.com/questions/25853722/how-to-suppress-binary-file-matching-results-in-grep

- https://stackoverflow.com/questions/10346816/using-grep-to-search-for-a-string-that-has-a-dot-in-it


Grepping ps output without showing the grep process
***************************************************************

- https://www.safaribooksonline.com/library/view/bash-cookbook/0596526784/ch17s18.html

- https://unix.stackexchange.com/questions/74185/how-can-i-prevent-grep-from-showing-up-in-ps-results

.. image::  ../source/images/utilities-grep-ps-output.png
    :width: 758px
    :align: center
    :height: 209px


######
FIND
######

*Some useful links to cover the working of Find*

- https://thevaluable.dev/find-cli-guide-examples/

- https://www.digitalocean.com/community/tutorials/how-to-use-find-and-locate-to-search-for-files-on-a-linux-vps
   
- https://tecadmin.net/delete-files-older-x-days/
   
- https://www.tecmint.com/find-and-sort-files-modification-date-and-time-in-linux/
   
- https://www.linode.com/docs/tools-reference/tools/find-files-in-linux-using-the-command-line

- https://alvinalexander.com/blog/post/linux-unix/find-how-multiple-search-patterns-filename-command

- https://stackoverflow.com/questions/5475905/linux-delete-file-with-size-0/18052644#18052644

.. image::  ../source/images/utilities-find-delete-empty-files.png
    :width: 748px
    :align: center
    :height: 351px


#######################
User Management
#######################

- https://www.linode.com/docs/tools-reference/linux-users-and-groups

- https://linux-audit.com/unused-linux-users-delete-or-keep/

- https://askubuntu.com/questions/515103/how-can-i-display-all-users-and-groups-with-a-command

.. image::  ../source/images/utilities-list-all-users-groups.png
    :width: 738px
    :align: center
    :height: 310px

- https://askubuntu.com/questions/34074/how-do-i-change-my-username

.. image::  ../source/images/utilities-change-username.png
    :width: 753px
    :align: center
    :height: 1049px


################
File Permissions
################

.. image::  ../source/images/linux-file-permissions.jpg
    :width: 800px
    :align: center
    :height: 696px
    :alt: Credits to ByteByteGo


- https://www.linux.com/learn/getting-know-linux-file-permissions
   
- https://www.penguintutor.com/linux/file-permissions-reference
   
- https://www.linux.com/learn/understanding-linux-file-permissions
   
- https://www.linuxnix.com/chmod-command-explained-linuxunix/
   
- https://unix.stackexchange.com/questions/21251/execute-vs-read-bit-how-do-directory-permissions-in-linux-work
   
- https://www.grymoire.com/Unix/Permissions.html
   
- https://www.thegeekstuff.com/2010/06/chmod-command-examples/
   
- https://danielmiessler.com/study/unixlinux_permissions/

- https://www.linux.com/learn/how-easily-back-and-restore-linux-file-permissions

- https://unix.stackexchange.com/questions/102286/ls-gives-no-such-file-or-directory-message


Why sudo cd <path-to-dir> doesn't work
***************************************************
- https://superuser.com/questions/241129/why-wont-sudo-cd-work

.. image::  ../source/images/utilities-sudo-cd-dir-1.png
    :width: 746px
    :align: center
    :height: 601px
        
- https://askubuntu.com/questions/291666/why-doesnt-sudo-cd-var-named-work

.. image::  ../source/images/utilities-sudo-cd-dir-2.png
    :width: 749px
    :align: center
    :height: 903px

- https://askubuntu.com/questions/468901/how-to-show-only-hidden-files-in-terminal/468902#468902

Sudoers
*************
- https://serverfault.com/questions/364334/test-whether-a-user-has-sudo-privileges-without-requiring-user-input
  
- https://www.digitalocean.com/community/tutorials/how-to-add-delete-and-grant-sudo-privileges-to-users-on-a-debian-vps
   
- https://www.thegeekstuff.com/2010/09/sudo-command-examples/
   
- https://www.garron.me/en/linux/visudo-command-sudoers-file-sudo-default-editor.html
   
- https://www.digitalocean.com/community/tutorials/how-to-edit-the-sudoers-file-on-ubuntu-and-centos

- https://askubuntu.com/questions/73864/how-to-modify-an-invalid-etc-sudoers-file

.. image::  ../source/images/utilities-fix-invalid-sudoers-file.png
    :width: 751px
    :align: center
    :height: 682px

- https://askubuntu.com/questions/799669/etc-sudoers-file-corrupted-and-i-cant-run-pkexec-visudo-over-ssh

.. image::  ../source/images/utilities-pksudo-visudo-invalid-sudoers.png
    :width: 748px
    :align: center
    :height: 396px
   
   
UserMod Command
**************************
- https://www.tecmint.com/usermod-command-examples/
   
- https://www.crybit.com/15-switches-of-usermod-command-with-example-unixlinux/
   
- https://muffinresearch.co.uk/linux-changing-uids-and-gids-for-user/
   
- https://www.smarthomebeginner.com/safely-change-primary-group-group-in-linux/
   
- https://www.cyberciti.biz/faq/howto-linux-add-user-to-group/


SetUID and SetGID
**************************
- https://tutonics.com/articles/linux-file-permissions-chmod-umask/
   
- https://www.slashroot.in/suid-and-sgid-linux-explained-examples

- https://www.thegeekstuff.com/2013/02/sticky-bit/

- https://www.linuxnix.com/suid-set-suid-linuxunix/

- https://unix.stackexchange.com/questions/28363/whats-the-difference-between-s-and-s-in-ls-la
   
UMask Values
************************
- → UMask contains default permissions for newly created files / directories based on base permissions for those
- → Base permissions for files is 666 (read-write permissions for owner-group-other : execute permissions are excluded by for files as security measure)
- → Similarly, the base permissions for directories are 777 (read-write-execute permissions for owner-group-other)
- → The UMask values are inverse to regular file permissions → i.e: chmod
- → UMask values = Base permissions - required permissions `All UMasks <https://www.linuxtrainingacademy.com/all-umasks/>`_
   
- https://www.computerhope.com/unix/uumask.htm

- https://www.cyberciti.biz/tips/understanding-linux-unix-umask-value-usage.html

- https://www.digitalocean.com/community/tutorials/linux-permissions-basics-and-how-to-use-umask-on-a-vps


##########
SymLinks
##########

*Some useful links to cover the working of SymLinks*

- https://www.cyberciti.biz/tips/understanding-unixlinux-symbolic-soft-and-hard-links.html
   
- https://www.thegeekstuff.com/2010/10/linux-ln-command-examples/

- https://geek-university.com/symbolic-links/
   
- https://geek-university.com/hard-links/


##########
Others
##########


XArgs vs Exec
*********************
   
- https://danielmiessler.com/blog/linux-xargs-vs-exec/

- https://stackoverflow.com/questions/16758525/make-xargs-handle-filenames-that-contain-spaces

.. image::  ../source/images/utilities-xargs-names-with-spaces-2.png
    :width: 720px
    :align: center
    :height: 545px


- https://askubuntu.com/questions/666001/piping-find-name-to-xargs-results-in-filenames-with-spaces-not-being-passed-to/666004

.. image::  ../source/images/utilities-xargs-names-with-spaces-1.png
    :width: 726px
    :align: center
    :height: 560px
 


NTP
**************
- https://support.ntp.org/Support/TroubleshootingNTP
   
- https://support.rackspace.com/how-to/using-ntp-to-sync-time/
   
- https://www.ibm.com/support/knowledgecenter/en/ssw_aix_71/com.ibm.aix.cmds4/ntpdate.htm
   

Renaming / Deleting multiple files
******************************************
- https://www.cyberciti.biz/tips/renaming-multiple-files-at-a-shell-prompt.html
   
- https://www.linux.com/blog/linux-shell-tip-remove-files-names-contains-spaces-and-special-characters-such

- https://www.cyberciti.biz/faq/linux-bash-delete-all-files-in-directory-except-few/
   
- https://www.tecmint.com/delete-all-files-in-directory-except-one-few-file-extensions/
   
- https://askubuntu.com/questions/470134/how-to-find-the-creation-time-of-a-file

- https://www.if-not-true-then-false.com/2011/linux-display-show-file-contents-tabs-line-breaks-non-printing-characters/


Rename multiple files with different extensions
********************************************************
- https://superuser.com/questions/865826/linux-mv-command-for-moving-multiple-files-with-different-extensions

.. image::  ../source/images/utilities-mv-diff-ext.png
    :width: 755px
    :align: center
    :height: 409px


Random Tools
******************
- https://aarvik.dk/blacklist-check-unix-linux-utility/

- https://www.tecmint.com/show-progress-linux-commands/

- https://www.tecmint.com/screen-command-examples-to-manage-linux-terminals/
   
- https://www.thegeekstuff.com/2009/04/chage-linux-password-expiration-and-aging/

- https://www.commandlinefu.com/commands/browse

- https://distrochooser.de/en

- https://www.cyberciti.biz/open-source/command-line-hacks/compgen-linux-command/

- https://www.dynacont.net/documentation/linux/Useful_SystemD_commands/


#######
SysCTL
#######

*Some useful links to cover the working of SysCTL*

- https://rtcamp.com/tutorials/linux/sysctl-conf
   
- https://www.cyberciti.biz/faq/linux-kernel-etcsysctl-conf-security-hardening

- https://www.slashroot.in/linux-network-tcp-performance-tuning-sysctl

- https://www.linux.com/news/kernel-tuning-sysctl


#######
LSOF
#######

- https://danielmiessler.com/study/lsof/
   
- https://catonmat.net/unix-utilities-lsof
   
- https://www.thegeekstuff.com/2012/08/lsof-command-examples/

- https://unix.stackexchange.com/questions/253321/how-to-display-size-human-readable-in-lsof-grep-var


##########
DIFF
##########
- https://www.lifewire.com/compare-two-text-files-linux-3861434

Comparing difference between files / directories on 2 servers
**********************************************************************
- https://www.xmodulo.com/how-to-diff-remote-files-over-ssh.html
