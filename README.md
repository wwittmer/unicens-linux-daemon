UNICENS DAEMON (unicensd)
To get it running, you will need to get cmake installed.
On debian based machines enter:
$ sudo apt-get install cmake

Perform this steps:
Enter:
$ ./build.sh

Now the binaries unicensd and xml2stuct shall be available in the root folder of unicensd project.
Make sure MOST Linux Driver is loaded (loadDriver.sh in "driver" folder).
The daemon needs to access these control enabled CDEVs:
/dev/inic-usb-crx
/dev/inic-usb-ctx

Make sure you have the rights to access these CDEVs (using sudo e.g.)
Launch daemon with the correct XML file, for example:
$ ./unicensd cfg/config_multichannel_audio_kit.xml &

To get a static C-based configuration enter:
$ ./xml2struct cfg/config_multichannel_audio_kit.xml > default_config.c
Afterwise build the daemon again:
$ ./build.sh