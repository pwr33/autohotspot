# autohotspot
linux (raspberry pi) create hotspot if local network not found

#!/bin/bash
# original script is from source referenced below
# the setup required is described on the web site below
# modified by Paul W. Rogers to deal with no values found by iw
# or cases where the desired ssid is not in results even though it is available
# 
# added some extra debug output
# also reindented to my preference, no tabs, 2 space indent
#
# pwr: to run from root crontab need PATH defined in the crontab
#
# version pwr: 0.99

#You may share this script on the condition a reference to RaspberryConnect.com 
#must be included in copies or derivatives of this script. 

#A script to switch between a wifi network and an Internet routed Hotspot
#A Raspberry Pi with a network port required for Internet in hotspot mode.
#Works at startup or with a seperate timer or manually without a reboot
#Other setup required find out more at
#http://www.raspberryconnect.com
