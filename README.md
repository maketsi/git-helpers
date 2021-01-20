## git-archive-this

Creates clean tgz archive of the current (git) directory (and branch), including the main
directory name in the package, and leaving out all git metadata.

Useful when you want to track subfolders in different GIT repositories and still easily
export them out with their main directory name included.


### Example use-case: Splunk addon development

* Splunk apps are located in <splunk>/etc/apps/<appname>/
* You want to track each addon in a separate GIT repository, while still being able to test them live.
* Create new addon directory and initialize it: mkdir testapp; cd testapp; git init
* from anywhere within the addon (sub)folders, call 'git-archive-this' to create an export
  package of the current active branch of the addon, storing it into <splunk>/etc/apps/appname.tgz
* upload the appname.tgz to an another splunk instance and it works correctly.

