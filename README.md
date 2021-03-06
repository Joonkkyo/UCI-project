# BP_Sensor

This code use [MetaWear Python SDK](https://github.com/mbientlab/MetaWear-SDK-Python)

__You can use only Linux environment__

# Install

The API metawear depends on [Warble](https://github.com/mbientlab/Warble) and Warble requires 3 installations

[bluez](www.bluez.org).   
Boost headers.   
GNU with a C++ compiler that support C++ 14.  

To use the bluez, First, the device files are installed and then, we have to install bluez. You can also use apt to get bluez-util as [Metawear tutorial on Linux](https://mbientlab.com/tutorials/Linux.html), but this way will cause some error. So, you have to use a makefile to install bluez

## On Ubuntu
    $ sudo apt-get update
    $ sudo apt-get install -y libusb-dev libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev
    $ tar xvf bluez-5.40.tar.xz
    $ cd bluez-5.40
    $ ./configure
    $ make
    $ sudo make install
    $ sudo apt-get install build-essential
    $ sudo apt-get install libboost-all-dev
    $ sudo apt-get install libbluetooth-dev
    $ pip -r install requirements.txt
    
## On Arch Linux
```shell script
    $ yay -S boost
    $ yay -S bluez
    $ yay -S bluez-util
    # systemctl enable bluetooth
    # systemctl start bluetooth
    $ bluetoothctl power on
    $ pip -r install requirements.txt
    $ sudo setcap 'cap_net_raw,cap_net_admin+eip' `which python`
    $ sudo setcap 'cap_net_raw,cap_net_admin+eip' `which hciconfig`
    $ sudo setcap 'cap_net_raw,cap_net_admin+eip' `which hcitool`
```

# PyGATTLib
```shell script
pip3 download gattlib
tar xvzf ./gattlib-0.20150805.tar.gz
cd gattlib-0.20150805/
sed -ie 's/boost_python-py34/boost_python3/' setup.py
pip3 install .
```
    
# Usage
If you execute this code, After finding the bluetooth device near our device, you can choose device which you want to connect

![original](https://media.github.uci.edu/user/1629/files/80d5cf80-b2ed-11e9-9451-93a25e901b81)
