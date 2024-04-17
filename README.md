# HackrfJAM_LXD
# INSTALLING HACKRFJAM ON LXD
```
lxc launch images:ubuntu/focal/amd64 HackrfJAM
```
```
lxc exec HackrfJAM -- bash
```
Have a look at [lte](https://github.com/SitrakaResearchAndPOC/Readme_hacklte/blob/main/hacklte_readme.txt)
```
apt update
```
```
apt-get install libjeromq-java libzmq-ffi-perl libzmq-java libzmq-java-doc libzmq-jni libzmq3-dev libzmq5 libzmqpp-dev libzmqpp4 python3-zmq python3-zmq libboost-dev libpython3.8-dev cmake build-essential python3-qwt python3-guiqwt python3-pyqt5.qwt libgmp-dev libxi-dev libcppunit-dev libx11-6 libx11-dev flex libncurses5 libncurses5-dev libncursesw6 libpcsclite-dev libsdl1.2-dev zlib1g-dev libmpfr6 libmpc3 lemon aptitude libtinfo-dev libtool shtool autoconf git-core pkg-config make libmpfr-dev python-cheetah libmpc-dev libtalloc-dev libfftw3-dev libgnutls28-dev libtool-bin python-lxml libxml2-dev python-sip sofia-sip-bin libsofia-sip-ua-dev sofia-sip-bin bison libgmp3-dev alsa-oss asn1c libdbd-sqlite3 libboost-all-dev libusb-1.0-0-dev python-mako python3-mako doxygen python-docutils cmake build-essential g++ python-numpy python3-numpy swig libsqlite3-dev libi2c-dev libwxgtk3.0-gtk3-dev freeglut3-dev composer phpunit python3-pip libfontconfig1-dev libxrender-dev python-sip-dev  libusb-dev libusb-1.0.0-dev libcomedi-dev libzmq3-dev javascript-common libjs-jquery libjs-sphinxdoc libjs-underscore python-sphinx-click-doc python-sphinx-copybutton-doc python-sphinx-feature-classification-doc python-sphinx-gallery-doc python-sphinxcontrib.bibtex-doc python-sphinxcontrib.programoutput-doc python-sphinxcontrib.spelling-doc build-essential libgmp-dev libx11-6 libx11-dev flex libncurses5 libncurses5-dev libncursesw6 libpcsclite-dev zlib1g-dev libmpfr6 libmpc3 lemon aptitude libtinfo-dev libtool shtool autoconf git-core pkg-config make libmpfr-dev libmpc-dev libtalloc-dev libfftw3-dev libgnutls28-dev  libtool-bin libxml2-dev sofia-sip-bin libsofia-sip-ua-dev sofia-sip-bin bison libgmp3-dev alsa-oss asn1c libdbd-sqlite3 libboost-all-dev libusb-1.0-0-dev python-mako python3-mako doxygen python-docutils cmake build-essential g++ python-numpy python3-numpy swig libsqlite3-dev libi2c-dev libwxgtk3.0-gtk3-dev freeglut3-dev composer phpunit python3-pip
```
Installing UHD
```
git clone https://github.com/ettusresearch/uhd
```
```
cd uhd/
```
```
git checkout aea0e2de34803d5ea8f25d7cf2fb08f4ab9d43f0
```
```
cd ..
```
```
zip -r uhd.zip uhd
```
#mv uhd.zip ../../Desktop/ltehack_backup 
```
cd uhd/host/ && mkdir build && cd build/
```
```
cmake ..
```
```
make
```
#make test
```
make install
```
```
ldconfig
```
```
cd ../../..
```
```
/usr/local/lib/uhd/utils/uhd_images_downloader.py
```
Installing SOAPY SDR
```
git clone https://github.com/pothosware/SoapySDR
```
```
cd SoapySDR/
```
```
git checkout f722f9ce5b629c3c44401a9bf628b3f8e67a9695
```
```
cd ..
```
```
zip -r SoapySDR.zip SoapySDR/
```
```
#mv SoapySDR.zip ../../Desktop/ltehack_backup 
```
```
cd SoapySDR && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
# INSTALLING GRC 38 + CLEVER JAM
```
sudo apt-get -y install autoconf automake build-essential ccache cmake cpufrequtils doxygen ethtool fort77 g++ gir1.2-gtk-3.0 git gobject-introspection gpsd gpsd-clients inetutils-tools libasound2-dev libboost-all-dev libcomedi-dev libcppunit-dev libfftw3-bin libfftw3-dev libfftw3-doc libfontconfig1-dev libgmp-dev libgps-dev libgsl-dev liblog4cpp5-dev libncurses5 libncurses5-dev libpulse-dev libqt5opengl5-dev libqwt-qt5-dev libsdl1.2-dev libtool libudev-dev libusb-1.0-0 libusb-1.0-0-dev libusb-dev libxi-dev libxrender-dev libzmq3-dev libzmq5 ncurses-bin python3-cheetah python3-click python3-click-plugins python3-click-threading python3-dev python3-docutils python3-gi python3-gi-cairo python3-gps python3-lxml python3-mako python3-numpy python3-numpy-dbg python3-opengl python3-pyqt5 python3-requests python3-scipy python3-setuptools python3-six python3-sphinx python3-yaml python3-zmq python3-ruamel.yaml swig wget
```
```
sudo apt-get install git cmake g++ libboost-all-dev libgmp-dev swig python3-numpy  python3-mako python3-sphinx python3-lxml doxygen libfftw3-dev  libsdl1.2-dev libgsl-dev libqwt-qt5-dev libqt5opengl5-dev python3-pyqt5  liblog4cpp5-dev libzmq3-dev python3-yaml python3-click python3-click-plugins python3-zmq python3-scipy python3-gi python3-gi-cairo gir1.2-gtk-3.0 libcodec2-dev libgsm1-dev libusb-1.0-0 libusb-1.0-0-dev libudev-dev
```
#/* </br>
#git log --since="2022-1-1" --until="2022-1-30" </br>
#git log --since="2021-1-1" --until="2021-1-10" </br>
#BEST PRECAUTION : </br>
https://wiki.gnuradio.org/index.php?title=ModuleNotFoundError#B._Finding_the_Python_library </br>
https://wiki.gnuradio.org/index.php/UbuntuInstall </br>
#THE VARIABLE HAS RED CROSS IN GRC, IT IS NOT ERROR ON UBUNTU </br>
#INSTALLING DEPENDENCIES + GNURADIO USING maint version + LOOK THE DATE </br>
#FINDING GR-OSMOSDR COMPATIBLE WITH GNURADIO + NEAR (<) THE DATE </br>
#ALL DEVICES (HACKRF) SHOULD BE NEAR (<) THE DATE OF GR-OSMOSDR  </br>
#COMPILING BY ORDER :  </br>
#DRIVER DEVICES -> SOAPYHACKRF ->  SOAPY_UHD -> GR-OSMOSDR </br>
</br>
#hackrf 10/12/2020 < 11/01/2021 :  </br>
#61a06b904dbf5e54da1d84473004db0472950487 </br>
#soapyhackrf 21/08/2020 < 11/01/2021 : </br>
#soapyhackrf : 7d530872f96c1cbe0ed62617c32c48ce7e103e1d </br>
#gr-osmosdr 11/01/2021 : cffef690f29e0793cd2d6c5d028c0c929115f0ac</br>
</br>
#INSTALLING GNURADIO maint-3.8 DATE :  </br>
#1Fevrier 2022 : maint-3.8 or 57bd109d5f0afdf09a3a52e226f464e8a71c5b82 </br>
#*/ </br>
``` 
mkdir grc38
```
```
cd grc38
```
Installing Driver Hackrf
```
git clone https://github.com/mossmann/hackrf.git
```
```
mv hackrf hackrf_grc38
```
```
cd hackrf_grc38
```
```
git checkout 61a06b904dbf5e54da1d84473004db0472950487
```
```
cd ..
```
```
zip -r hackrf_grc38.zip hackrf_grc38
```
#mv hackrf_grc38.zip ../../Desktop/ltehack_backup/
```
cd hackrf_grc38/host && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../../..
```
Installing SoaphHackrf
```
git clone https://github.com/pothosware/SoapyHackRF.git
```
```
cd SoapyHackRF/
```
```
git checkout 7d530872f96c1cbe0ed62617c32c48ce7e103e1d
```
```
cd ..
```
```
mv SoapyHackRF SoapyHackRF_grc38
```
```
zip -r SoapyHackRF_grc38.zip SoapyHackRF_grc38
```
#mv SoapyHackRF_grc38.zip ../../Desktop/ltehack_backup/
```
cd SoapyHackRF_grc38 && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
#PLUG HACKRF
#Test : 
```
hackrf_info
```
```
SoapySDRUtil --info
```
#Available factories...hackrf, null,
```
SoapySDRUtil --probe="driver=hackrf"
```
```
SoapySDRUtil --make="driver=hackrf"
```

Installing SoapyUHD
```
git clone https://github.com/pothosware/SoapyUHD
```
```
cd SoapyUHD/
```
```
git checkout 47972ba8b96beffb79915e300acea168bacd8d84
```
```
cd ..
```
```
mv SoapyUHD SoapyUHD_grc38
```
```
zip -r SoapyUHD_grc38.zip SoapyUHD_grc38
```
#mv SoapyUHD_grc38.zip ../../Desktop/ltehack_backup/
```
cd SoapyUHD_grc38 && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
#Test :
```
uhd_usrp_probe
```
#https://wiki.gnuradio.org/index.php/UbuntuInstall
#https://wiki.gnuradio.org/index.php?title=LinuxInstall#From_Source
#https://github.com/gnuradio/volk/issues/340
```
apt-get update && apt-get clean && apt-get autoremove && apt-get install -y apt-utils
```
```
apt-get install -y build-essential cmake git pkg-config python3-mako python3-numpy python3-distutils gcc-9 g++-9 gdb
```
Installing GNURADIO 3.8
```
git clone https://github.com/gnuradio/gnuradio
```
```
mv gnuradio gnuradio_38
```
```
cd gnuradio_38
```
```
git checkout maint-3.8  
```
#git pull --recurse-submodules=on
#git submodule update --init

```
git submodule init && git submodule update
```
```
cd ..
```
```
zip -r  gnuradio_38.zip  gnuradio_38
```
#mv gnuradio_38.zip ../../Desktop/ltehack_backup/
```
cd gnuradio_38 && mkdir build && cd build
```
```
cmake -DCMAKE_BUILD_TYPE=Release -DPYTHON_EXECUTABLE=/usr/bin/python3.8 ../
```
```
make 
```
```
make test
```
```
make install
```
```
ldconfig
```
```
export PYTHONPATH=/usr/local/lib/python3/dist-packages:/usr/local/lib/python3.8/dist-packages:$PYTHONPATH
```
```
export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH
```
```
cd ../..
```
TEST GNURADIO COMPAGNION
```
gnuradio-companion
```
Installing gr-osmosdr
```
git clone https://github.com/osmocom/gr-osmosdr
```
```
cd gr-osmosdr/
```
```
git checkout cffef690f29e0793cd2d6c5d028c0c929115f0ac
```
```
cd ..
```
```
mv gr-osmosdr gr-osmosdr_grc38
```
```
zip -r gr-osmosdr_grc38.zip gr-osmosdr_grc38
```
#mv gr-osmosdr_grc38.zip ../../Desktop/ltehack_backup/
```
cd gr-osmosdr_grc38 && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
```
cd ..
```
Installing cleverJAM
```
git clone https://github.com/SitrakaResearchAndPOC/fork_CleverJAM
```
```
zip -r CleverJAM.zip CleverJAM/
```
#mv CleverJAM.zip ../Desktop/ltehack_backup/
```
cd CleverJAM/sources
```
#RUN GNURADIO COMPANION + FILE AND OPEN jam.grc + SET CORRECT FREQUENCY
```
gnuradio-companion
```

#USE "LTE DISCOVERY" OR "NETWORK SIGNAL GURU"  </br>
#OR USE CODE USSD : *#*#4636#*#* on ANDROID </br>
#OR USE CODE USSD : *#0011# on SAMSUNG </br>
#OR USE CODE USSD : *300#12345#* on I-PHONE </br>

#Clever jam could run with hopping frequency using python script </br>
#regards read me cleverjam for test </br>
</br>
FLASHING FIRMEWARE HACKRF </br>
#FLASHING HACKRF WITH NEW FIRMWARE </br>
```
wget https://github.com/greatscottgadgets/hackrf/releases/download/v2023.01.1/hackrf-2023.01.1.tar.xz
```
```
tar -xvf hackrf-2023.01.1.tar.xz
```
```
mv hackrf-2023.01.1.tar.xz ../../Desktop/ltehack_backup 
```
```
cd hackrf-2023.01.1/firmware-bin/
```
#PRESS DFU AND RESET
```
hackrf_spiflash -w hackrf_one_usb.bin
```
#PRESS RESET </br>
#apt-get install dfu-util </br>
#dfu-util -D hackrf_one_usb.dfu </br>
</br>
#Test : plug hackrf </br>
```
hackrf_info
```
```
SoapySDRUtil --info
```
```
exit
```

# INSTALLING PROFILE 
Have a look at [profile](https://documentation.ubuntu.com/lxd/en/latest/profiles/) or [pdf_profile](https://github.com/SitrakaResearchAndPOC/HackrfJAM_LXD/blob/main/How%20to%20use%20profiles%20-%20Canonical%20LXD%20documentation.pdf)
INSTALL ON REAL MACHINE NOT THE CONTAINER
```
apt udpate
```
```
apt-get install nano 
```
Paste this file
```
config:
  environment.DISPLAY: :0
  raw.idmap: both 1000 1000
description: GUI LXD profile
devices:
  X0:
    path: /tmp/.X11-unix/X0
    source: /tmp/.X11-unix/X0
    type: disk
  my_gpu:
    type: gpu
name: gui
```
SAVE THE FILE as .gui.txt </br>
Create the profile
```
lxc profile create gui
```
```
lxc profile edit gui < .gui.txt
```
```
rm .gui.txt
```
```
lxc profile add HackrfJAM gui
```
```
lxc config set HackrfJAM security.privileged=true
```
```
lxc start HackrfJAM
```
```
lxc exec HackrfJAM -- bash
```
Testing GUI Firefox
```
apt update
```
```
apt-get install firefox
```
```
firefox
```
# PROBLEM OF DISPLAY
Problem display at [display](https://bbs.archlinux.org/viewtopic.php?id=221449) or [pdf_display](https://github.com/SitrakaResearchAndPOC/HackrfJAM_LXD/blob/main/How%20to%20resolve%20%E2%80%9CNo%20protocol%20specified%20Unable%20to%20init%20server__%20%5BSolved%5D%20_%20Newbie%20Corner%20_%20Arch%20Linux%20Forums.pdf) </br>

* reboot the real machine :
```
rm -rf /tmp/.X11-unix/X*
```
```
reboot
```
* please reboot the container images : 
```
lxc stop  HackrfJAM
```
```
lxc start HackrfJAM
```
* listing the profile
```
lxc profile list
```
* adding the profile
```
lxc profile add HackrfJAM gui
```
* Please verify if there are two x0 and choose following ;
You could verify using
```
lsof -U | grep X1
```
```
chmod +x /tmp/.X11-unix/X0
```
```
xhost +local:
```
```
pgrep -a X
```
```
echo $DISPLAY
```
```
echo $TERM
```
* IF PROBLEM PERSIST
```
lxc profile edit gui
```
Change as
```
config:
  environment.DISPLAY: :1
  raw.idmap: both 1000 1000
description: GUI LXD profile
devices:
  X1:
    path: /tmp/.X11-unix/X1
    source: /tmp/.X11-unix/X1
    type: disk
  my_gpu:
    type: gpu
name: gui
```
* remak all step on the PROBLEM OF DISPLAY
* if problem still persists ; change by other number

# SAVING FINAL IMAGE :

* OLD VERSION [IMAGE]()
```
lxc publish HackrfJAM --alias HackrfJAM -f
```
Instance published with fingerprint: 4406e78ba577089a930fd9bb7ae92ffb494c321fd39ba9cbfdcc1ce23a6ccd1f
```
lxc image export HackrfJAM .
```
```
md5sum 4406e78ba577089a930fd9bb7ae92ffb494c321fd39ba9cbfdcc1ce23a6ccd1f.tar.gz
```
c5c03fd9b7a33b1689a3dab9df2fabd6  4406e78ba577089a930fd9bb7ae92ffb494c321fd39ba9cbfdcc1ce23a6ccd1f.tar.gz
```
chmod 777 4406e78ba577089a930fd9bb7ae92ffb494c321fd39ba9cbfdcc1ce23a6ccd1f.tar.gz
```

* NEW VERSION (IMAGE)[]
```
lxc publish HackrfJAM --alias HackrfJAM -f
```
Instance published with fingerprint: 3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211
```
lxc image export HackrfJAM .
```
```
md5sum 3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211.tar.gz
```
ed2381fd28cc9e452cb2447770ce1a32  3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211.tar.gz
```
chmod 777 3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211.tar.gz
```





# HackrfJAM FOR QUICK INSTALL
## Installation with LXC  using ubuntu if not yet installed
```
apt update
```
```
apt-get install lxd lxd-client
```


## Installation with LXC  using DragonOS if not yet installed
```
apt update
```
```
apt-get install snapd  
```
```
snap install lxd  
```

```
snap install lxd-client  
```

## Initialisation of LXD if not yet installed
```
lxd init  
```
For questions please follow the default option, an image illustration is at [image](https://github.com/SitrakaResearchAndPOC/QCSuper/blob/main/screen.jpg) 
  
User need to be in group lxd :
```
sudo usermod -a G lxd $USER  
```
or  
```
sudo /usr/sbin/usermod lxd $USER  
```

$PATH need to contains /usr/local/bin, verify with :  
```
echo $PATH  
```

if not, setup this, or add this in your .bashrc or .zshrc or ...  

```
export PATH=$PATH:/usr/local/bin  
```
# IMPORTING IMAGES FOR QUICK INSTALL
## downloading and importing image for Quick install
OVAINA
```
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1yYLVjgxRSxJlRqznnWTs0LUKTQzZKqZf' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1yYLVjgxRSxJlRqznnWTs0LUKTQzZKqZf" -O 3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211.tar.gz   && rm -rf /tmp/cookies.txt  
```
```
lxc image import 3b1b00e67439adbe6d6228dc9fd9e05c1463bbafd64b2e0438bcb499e8274211.tar.gz --alias HackrfJAMimage
```
```
lxc launch HackrfJAMimage HackrfJAM
```

# LAUNCHING FOR QUICK INSTALL
## Finding all devices
```
lsusb
```
## Adding devices USRP on LXC for Quick install
```
wget https://raw.githubusercontent.com/SitrakaResearchAndPOC/fork_QCSuperLXD/main/lxd-device
```
```
chmod +x lxd-device
```
```
sudo cp lxd-device /usr/local/bin
```
```
lxd-device add HackrfJAM hackrf
```
Plug hackrf devices
```
lxc exec HackrfJAM -- uhd_images_downloader
```
```
lxc exec HackrfJAM --  uhd_usrp_probe 
```
```
lxc exec HackrfJAM -- uhd_find_devices 
```
```
lxc exec HackrfJAM -- bash
```

## Setting privileges for Quick install
```
lxc config set HackrfJAM security.privileged=true
```


## launching for Quick install
```
lxc exec HackrfJAM -- bash
```
```
exit
```
# installing profile for quick install 
Have a look at [profile](https://documentation.ubuntu.com/lxd/en/latest/profiles/) or [pdf_profile](https://github.com/SitrakaResearchAndPOC/HackrfJAM_LXD/blob/main/How%20to%20use%20profiles%20-%20Canonical%20LXD%20documentation.pdf)
INSTALL ON REAL MACHINE NOT THE CONTAINER
```
apt update
```
```
apt-get install nano 
```
Paste this file
```
config:
  environment.DISPLAY: :0
  raw.idmap: both 1000 1000
description: GUI LXD profile
devices:
  X0:
    path: /tmp/.X11-unix/X0
    source: /tmp/.X11-unix/X0
    type: disk
  my_gpu:
    type: gpu
name: gui
```
SAVE THE FILE as .gui.txt </br>
Create the profile
```
lxc profile create gui
```
```
lxc profile edit gui < .gui.txt
```
```
rm .gui.txt
```
```
lxc profile add HackrfJAM gui
```
```
lxc config set HackrfJAM security.privileged=true
```
```
lxc start HackrfJAM
```
```
lxc exec HackrfJAM -- bash
```
Testing GUI Firefox
```
firefox
```
## Problem of display for Quick install
Problem display at [display](https://bbs.archlinux.org/viewtopic.php?id=221449) or [pdf_display](https://github.com/SitrakaResearchAndPOC/HackrfJAM_LXD/blob/main/How%20to%20resolve%20%E2%80%9CNo%20protocol%20specified%20Unable%20to%20init%20server__%20%5BSolved%5D%20_%20Newbie%20Corner%20_%20Arch%20Linux%20Forums.pdf) </br>

* reboot the real machine :
```
rm -rf /tmp/.X11-unix/X*
```
```
reboot
```
* please reboot the container images : 
```
lxc stop  HackrfJAM
```
```
lxc start HackrfJAM
```
* listing the profile
```
lxc profile list
```
* adding the profile
```
lxc profile add HackrfJAM gui
```
* Please verify if there are two x0 and choose following ; 
```
chmod +x /tmp/.X11-unix/X0
```
```
xhost +local:
```
```
pgrep -a X
```
```
echo $DISPLAY
```
```
echo $TERM
```
* IF PROBLEM PERSIST
```
lxc profile edit gui
```
Change the number of dispaly as on the command echo $DISPLAY
```
config:
  environment.DISPLAY: :1
  raw.idmap: both 1000 1000
description: GUI LXD profile
devices:
  X1:
    path: /tmp/.X11-unix/X1
    source: /tmp/.X11-unix/X1
    type: disk
  my_gpu:
    type: gpu
name: gui
```
* remak all step on the PROBLEM OF DISPLAY
* if problem still persists ; change by other number and look at : </br> [link1](https://bbs.archlinux.org/viewtopic.php?id=221449) </br>[link2](https://bbs.archlinux.org/viewtopic.php?id=272491)  </br> [link3](https://bbs.archlinux.org/viewtopic.php?id=270585) </br> [link4](https://bbs.archlinux.org/viewtopic.php?id=281572) </br> [link5](https://bbs.archlinux.org/viewtopic.php?id=288581) </br>

  
## Testing jammer
lxc exec HackrfJAM -- gnuradio-companion

