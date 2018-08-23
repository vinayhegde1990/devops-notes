<h1>Getting Started</h1>

<h4> This document will show you how to create a Staging environment to work with Sphinx & Read the Docs </h4>

1. Assuming you have Python already, install Sphinx:

```bash
sudo pip install sphinx sphinx-autobuild
```

2. Create a directory inside your project to hold your docs:

```bash
cd /path/to/project
mkdir docs
```

3. Run sphinx-quickstart in there:

```bash
cd docs
sphinx-quickstart
```

4. This quick start will walk you through creating the basic configuration; in most cases, you can just accept the defaults. When it's done, you'll have an *index.rst*, a *conf.py* and some other files. Add these to revision control. Now, edit your *index.rst* and add some information about your project. Include as much detail as you like. Build them to see how they look:	

```
make html
```

**Note:** *You can use sphinx-autobuild to auto-reload your docs. Run sphinx-autobuild . _build/html instead.*


5. Edit your files to rebuild until you like what you see, then commit your changes and push to your public repository. Once you have **Sphinx** documentation in a public repository, you can start using **Read the Docs**.
