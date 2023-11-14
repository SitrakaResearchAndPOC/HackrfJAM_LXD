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
 


