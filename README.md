For Kernel 4.15.x ~ 5.4.x (Linux Mint or Ubuntu or All Debian Derivatives)
tested on debian 10 buster with signed kernel 5.4.x & kernel 4.19.x
------------------

## How to install

`sudo apt-get install build-essential git dkms linux-headers-$(uname -r)`

`git clone https://github.com/kelebek333/rtl8188fu`

`sudo dkms add ./rtl8188fu`

`sudo dkms build rtl8188fu/1.0`

`sudo dkms install rtl8188fu/1.0`

`sudo cp ./rtl8188fu/firmware/rtl8188fufw.bin /lib/firmware/rtlwifi/`

------------------

Run following commands for disable power management and plugging/replugging issues.

`sudo mkdir -p /etc/modprobe.d/`

`sudo touch /etc/modprobe.d/rtl8188fu.conf`

`echo "options rtl8188fu rtw_power_mgnt=0 rtw_enusbss=0" | sudo tee /etc/modprobe.d/rtl8188fu.conf`

------------------

## How to uninstall

`sudo dkms remove rtl8188fu/1.0 --all`

`sudo rm -f /lib/firmware/rtlwifi/rtl8188fufw.bin`

`sudo rm -f /etc/modprobe.d/rtl8188fu.conf`


------------------

## How to install from PPA repository

You can install rtl81188fu driver with following commands from PPA.

xUbuntu 16.04-19.10 / Linux Mint 18.x-19.x 

`sudo add-apt-repository ppa:kelebek333/kablosuz`

`sudo apt-get update`

`sudo apt install rtl8188fu-dkms`


You can purge packages with following commands

`sudo apt purge rtl8188fu-dkms`
##optional direct kernel build 
ttps://hardikpatelblogs-wordpress-com.cdn.ampproject.org/v/s/hardikpatelblogs.wordpress.com/2010/11/19/8/amp/?amp_js_v=a3&amp_gsa=1&usqp=mq331AQCKAE%3D#aoh=15810704616834&referrer=https%3A%2F%2Fwww.google.com&amp_tf=From%20%251%24s&ampshare=https%3A%2F%2Fhardikpatelblogs.wordpress.com%2F2010%2F11%2F19%2F8%2F
