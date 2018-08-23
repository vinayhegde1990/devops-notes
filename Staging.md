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



Sign Up and Connect an External Account
========================================
- If you are going to import a repository from GitHub, Bitbucket or GitLab, you should connect your account to your provider first. 
- Connecting your account allows for easier importing and enables Read the Docs to configure your repository webhooks automatically.
- To connect your account, go to your **Settings** dashboard and select **Connected Services**. From here, you will be able to connect to your GitHub, Bitbucket or GitLab account. 
- This process will ask you to authorize a connection to Read the Docs, that allows us to read information about and clone your repositories.



Import Your Docs
========================================
To import a repository, visit your [**dashboard**](https://readthedocs.org/dashboard) and click Import.

- If you have a connected account, you will see a list of your repositories that can be imported.
- To import one of these, just click the import icon next to the **repository** you would like to import. 
- This will bring up a form that is already filled with your project information. 
- Feel free to edit any of these properties, and the click Next to build your documentation.
