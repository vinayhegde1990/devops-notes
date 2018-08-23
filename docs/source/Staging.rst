.. _STAGING:

Staging
===========

.. Note:: This document will show you how to create a Staging environment to work with Sphinx & Read the Docs.


1. Assuming you have Python already, install Sphinx:

.. code-block:: python
   :linenos: 
   
   sudo pip install sphinx sphinx-autobuild
        

2. Create a directory inside your project to hold your docs:

.. code-block:: bash
    :linenos: 
   
    cd /path/to/project
    mkdir docs
        
        
3. Run sphinx-quickstart in there:

.. code-block:: bash
   :linenos: 
   
   cd docs
   sphinx-quickstart

        
4. This quick start will walk you through creating the basic configuration; in most cases, you can just accept the defaults. When it's done, you'll have an index.rst, a conf.py and some other files. Add these to revision control. Now, edit your index.rst and add some information about your project. Include as much detail as you like. Build them to see how they look:

.. code-block:: bash
   :linenos: 
       
   make html
        
.. Note::  You can use sphinx-autobuild to auto-reload your docs. Run sphinx-autobuild . _build/html instead.


5. To publish only relevant files but NOT the build, _static & _templates directories - please add a .gitignore in the root directory. A sample is below

.. code-block:: bash
   :linenos:

   #Folders to ignore
   build
   _templates
   _static

   #Extensions to ignore
   *.pyc
   *.diff
   *.err
   *.orig
   *.rej
 

6. Edit your files to rebuild until you like what you see, then commit your changes and push to your public repository. Once you have **Sphinx** documentation in a public repository, you can start using **Read the Docs**.
