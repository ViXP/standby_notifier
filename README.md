# STANDBY NOTIFIER
### Sites inaccessibility notification tool (daemon)
This tool will send the email to the specified address, if specified sites are
not answering with correct (200) status.

## Using
The application supports these commands:
`notifier -p PIDFILE_ADDRESS` - starts the standby notifier (restarts on the
second run)
`notifier stop -p PIDFILE_ADDRESS` - stops the standby notifier

* If *Pidfile* option is not specified - the process identifier will be saved inside
the current context, in the file called `process.pid`.

* The optional parameter `--nd` can be specified if you not wish to daemonize this
application.

* **URLs to monitor and email address for notifications can be configured 
inside the notifier executable file.**

## Installing as a service
If you wish to install it as the service (sudo privileges required), please, use

`sudo ./INSTALL_LINUX` - for Linux **Ubuntu OS** family

`sudo ./INSTALL_MACOS` - for **MacOS**

The service will be linked within the directory which is used in context of the
installation script (aka. current directory).