sensu-pkgbuild
==============

Sensu Omnibus PKGBUILD for ArchLinux

Omnibus version of Sensu, the open source monitoring framework. Direct from the .deb

Tested and working perfectly on my ArchLinux dedicated server, though monitoring just 1-2 boxes.

After building and installing, refer to /usr/share/sensu/systemd/README.md for information on the best way to control the Sensu daemons.  
**Note:** Sensu-ctl still has a sensu-dashboard daemon, but don't try to start it up as Uchiwa has replaced it as the supported dashboard. 
