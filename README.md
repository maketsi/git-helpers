## git-archive-this

Creates clean tgz archive export from the current GIT repository branch, including the base
directory name in the package. Leaves out all git metadata, being production ready.

If your .git repository is in a/b/.git, this will will create a package in a/b.tgz that has b/* in it.

Example use-case: Splunk addon development and production migration

* Splunk apps are located in ```<splunk>/etc/apps/<appname>/```
* You want to track each addon app in a separate GIT repository, while still being able to test them live.
* Create new app directory and initialize it: mkdir testapp; cd testapp; git init
* Make changes to the app and commit them
* Call ```git-archive-this``` from anywhere within the addon (sub)folders to create an export of the current branch.
  New export is stored (overridden) in ```<splunk>/etc/apps/appname.tgz```
* upload file ```appname.tgz``` to an another splunk instance using its GUI and it works correctly, having the same directory structure.


## git-basepath

Prints out the base path of the current GIT repository you are in.


## git-ls

Prints out a list of committed files from the current branch you are in. 

