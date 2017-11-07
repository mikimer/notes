
Here's the full linux that led up to Mike's error

```
pi@raspi:~ $ 
pi@raspi:~ $ pwd
/home/pi
pi@raspi:~ $ ls
Desktop  Documents  Downloads  Music  Pictures  Public  python_games  Templates  Videos
pi@raspi:~ $ raspi-config
Script must be run as root. Try 'sudo raspi-config'
pi@raspi:~ $ sudo raspi-config
pi@raspi:~ $ 
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get update
Hit:1 http://archive.raspberrypi.org/debian stretch InRelease
Hit:2 http://mirrordirector.raspbian.org/raspbian stretch InRelease      
Reading package lists... Done                                            
pi@raspi:~ $ sudo apt-get install git
Reading package lists... Done
Building dependency tree       
Reading state information... Done
git is already the newest version (1:2.11.0-3+deb9u2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get install git

Reading package lists... Done
Building dependency tree       
Reading state information... Done
git is already the newest version (1:2.11.0-3+deb9u2).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
pi@raspi:~ $ 
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get install python-pip
Reading package lists... Done
Building dependency tree       
Reading state information... Done
python-pip is already the newest version (9.0.1-2+rpt1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get install pkg-config libboost-python-dev libboost-thread-dev libbluetooth-dev libglib2.0-dev python-dev build-essential python-dev
Reading package lists... Done
Building dependency tree       
Reading state information... Done
build-essential is already the newest version (12.3).
pkg-config is already the newest version (0.29-4).
python-dev is already the newest version (2.7.13-2).
python-dev set to manually installed.
The following additional packages will be installed:
  libboost-atomic1.62-dev libboost-atomic1.62.0 libboost-chrono1.62-dev libboost-chrono1.62.0
  libboost-date-time1.62-dev libboost-python1.62-dev libboost-python1.62.0
  libboost-serialization1.62-dev libboost-serialization1.62.0 libboost-system1.62-dev
  libboost-thread1.62-dev libboost1.62-dev libpcre3-dev libpcre32-3 libpcrecpp0v5
Suggested packages:
  libboost1.62-doc gccxml libboost-context1.62-dev libboost-coroutine1.62-dev
  libboost-exception1.62-dev libboost-fiber1.62-dev libboost-filesystem1.62-dev
  libboost-graph1.62-dev libboost-graph-parallel1.62-dev libboost-iostreams1.62-dev
  libboost-locale1.62-dev libboost-log1.62-dev libboost-math1.62-dev libboost-mpi1.62-dev
  libboost-mpi-python1.62-dev libboost-program-options1.62-dev libboost-random1.62-dev
  libboost-regex1.62-dev libboost-signals1.62-dev libboost-test1.62-dev libboost-timer1.62-dev
  libboost-type-erasure1.62-dev libboost-wave1.62-dev libboost1.62-tools-dev libmpfrc++-dev
  libntl-dev libglib2.0-doc
The following NEW packages will be installed:
  libbluetooth-dev libboost-atomic1.62-dev libboost-atomic1.62.0 libboost-chrono1.62-dev
  libboost-chrono1.62.0 libboost-date-time1.62-dev libboost-python-dev libboost-python1.62-dev
  libboost-python1.62.0 libboost-serialization1.62-dev libboost-serialization1.62.0
  libboost-system1.62-dev libboost-thread-dev libboost-thread1.62-dev libboost1.62-dev
  libglib2.0-dev libpcre3-dev libpcre32-3 libpcrecpp0v5
0 upgraded, 19 newly installed, 0 to remove and 0 not upgraded.
Need to get 11.8 MB of archives.
After this operation, 134 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libpcrecpp0v5 armhf 2:8.39-3 [149 kB]
Get:2 http://archive.raspberrypi.org/debian stretch/main armhf libbluetooth-dev armhf 5.43-2+rpt2+deb9u2 [181 kB]
Get:3 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost1.62-dev armhf 1.62.0+dfsg-4 [7,009 kB]
Get:4 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-atomic1.62.0 armhf 1.62.0+dfsg-4 [31.1 kB]
Get:5 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-atomic1.62-dev armhf 1.62.0+dfsg-4 [29.5 kB]
Get:6 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-chrono1.62.0 armhf 1.62.0+dfsg-4 [35.7 kB]
Get:7 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-chrono1.62-dev armhf 1.62.0+dfsg-4 [37.4 kB]
Get:8 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-serialization1.62.0 armhf 1.62.0+dfsg-4 [105 kB]
Get:9 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-serialization1.62-dev armhf 1.62.0+dfsg-4 [170 kB]
Get:10 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-date-time1.62-dev armhf 1.62.0+dfsg-4 [51.1 kB]
Get:11 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-python1.62.0 armhf 1.62.0+dfsg-4 [120 kB]
Get:12 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-python1.62-dev armhf 1.62.0+dfsg-4 [156 kB]
Get:13 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-python-dev armhf 1.62.0.1+b4 [4,086 B]
Get:14 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-system1.62-dev armhf 1.62.0+dfsg-4 [33.1 kB]
Get:15 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-thread1.62-dev armhf 1.62.0+dfsg-4 [71.3 kB]
Get:16 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libboost-thread-dev armhf 1.62.0.1+b4 [3,724 B]
Get:17 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libpcre32-3 armhf 2:8.39-3 [227 kB]
Get:18 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libpcre3-dev armhf 2:8.39-3 [565 kB]
Get:19 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libglib2.0-dev armhf 2.50.3-2 [2,775 kB]
Fetched 11.8 MB in 9s (1,238 kB/s)                                                              
Selecting previously unselected package libpcrecpp0v5:armhf.
(Reading database ... 122776 files and directories currently installed.)
Preparing to unpack .../00-libpcrecpp0v5_2%3a8.39-3_armhf.deb ...
Unpacking libpcrecpp0v5:armhf (2:8.39-3) ...
Selecting previously unselected package libboost1.62-dev:armhf.
Preparing to unpack .../01-libboost1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-atomic1.62.0:armhf.
Preparing to unpack .../02-libboost-atomic1.62.0_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-atomic1.62.0:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-atomic1.62-dev:armhf.
Preparing to unpack .../03-libboost-atomic1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-atomic1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-chrono1.62.0:armhf.
Preparing to unpack .../04-libboost-chrono1.62.0_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-chrono1.62.0:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-chrono1.62-dev:armhf.
Preparing to unpack .../05-libboost-chrono1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-chrono1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-serialization1.62.0:armhf.
Preparing to unpack .../06-libboost-serialization1.62.0_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-serialization1.62.0:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-serialization1.62-dev:armhf.
Preparing to unpack .../07-libboost-serialization1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-serialization1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-date-time1.62-dev:armhf.
Preparing to unpack .../08-libboost-date-time1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-date-time1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-python1.62.0.
Preparing to unpack .../09-libboost-python1.62.0_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-python1.62.0 (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-python1.62-dev.
Preparing to unpack .../10-libboost-python1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-python1.62-dev (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-python-dev.
Preparing to unpack .../11-libboost-python-dev_1.62.0.1+b4_armhf.deb ...
Unpacking libboost-python-dev (1.62.0.1+b4) ...
Selecting previously unselected package libboost-system1.62-dev:armhf.
Preparing to unpack .../12-libboost-system1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-system1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-thread1.62-dev:armhf.
Preparing to unpack .../13-libboost-thread1.62-dev_1.62.0+dfsg-4_armhf.deb ...
Unpacking libboost-thread1.62-dev:armhf (1.62.0+dfsg-4) ...
Selecting previously unselected package libboost-thread-dev:armhf.
Preparing to unpack .../14-libboost-thread-dev_1.62.0.1+b4_armhf.deb ...
Unpacking libboost-thread-dev:armhf (1.62.0.1+b4) ...
Selecting previously unselected package libpcre32-3:armhf.
Preparing to unpack .../15-libpcre32-3_2%3a8.39-3_armhf.deb ...
Unpacking libpcre32-3:armhf (2:8.39-3) ...
Selecting previously unselected package libpcre3-dev:armhf.
Preparing to unpack .../16-libpcre3-dev_2%3a8.39-3_armhf.deb ...
Unpacking libpcre3-dev:armhf (2:8.39-3) ...
Selecting previously unselected package libglib2.0-dev.
Preparing to unpack .../17-libglib2.0-dev_2.50.3-2_armhf.deb ...
Unpacking libglib2.0-dev (2.50.3-2) ...
Selecting previously unselected package libbluetooth-dev.
Preparing to unpack .../18-libbluetooth-dev_5.43-2+rpt2+deb9u2_armhf.deb ...
Unpacking libbluetooth-dev (5.43-2+rpt2+deb9u2) ...
Setting up libboost-serialization1.62.0:armhf (1.62.0+dfsg-4) ...
Setting up libbluetooth-dev (5.43-2+rpt2+deb9u2) ...
Setting up libboost1.62-dev:armhf (1.62.0+dfsg-4) ...
Processing triggers for libglib2.0-0:armhf (2.50.3-2) ...
Setting up libboost-serialization1.62-dev:armhf (1.62.0+dfsg-4) ...
Processing triggers for libc-bin (2.24-11+deb9u1) ...
Setting up libboost-system1.62-dev:armhf (1.62.0+dfsg-4) ...
Setting up libboost-atomic1.62.0:armhf (1.62.0+dfsg-4) ...
Processing triggers for man-db (2.7.6.1-2) ...
Setting up libpcrecpp0v5:armhf (2:8.39-3) ...
Setting up libpcre32-3:armhf (2:8.39-3) ...
Setting up libboost-python1.62.0 (1.62.0+dfsg-4) ...
Setting up libboost-chrono1.62.0:armhf (1.62.0+dfsg-4) ...
Setting up libboost-atomic1.62-dev:armhf (1.62.0+dfsg-4) ...
Setting up libboost-date-time1.62-dev:armhf (1.62.0+dfsg-4) ...
Setting up libpcre3-dev:armhf (2:8.39-3) ...
Setting up libboost-python1.62-dev (1.62.0+dfsg-4) ...
Setting up libboost-chrono1.62-dev:armhf (1.62.0+dfsg-4) ...
Setting up libglib2.0-dev (2.50.3-2) ...
Setting up libboost-thread1.62-dev:armhf (1.62.0+dfsg-4) ...
Setting up libboost-python-dev (1.62.0.1+b4) ...
Setting up libboost-thread-dev:armhf (1.62.0.1+b4) ...
Processing triggers for libc-bin (2.24-11+deb9u1) ...
pi@raspi:~ $ 
pi@raspi:~ $ pip install pygatt
Collecting pygatt
  Downloading pygatt-3.2.0.tar.gz
Collecting enum-compat (from pygatt)
  Downloading enum-compat-0.0.2.tar.gz
Collecting pyserial (from pygatt)
  Downloading pyserial-3.4-py2.py3-none-any.whl (193kB)
    100% |████████████████████████████████| 194kB 793kB/s 
Collecting enum34 (from enum-compat->pygatt)
  Downloading enum34-1.1.6-py2-none-any.whl
Building wheels for collected packages: pygatt, enum-compat
  Running setup.py bdist_wheel for pygatt ... done
  Stored in directory: /home/pi/.cache/pip/wheels/6d/fa/b7/f916c29709510d1bb456a663be418585793d1f3ac1c1ef6e8f
  Running setup.py bdist_wheel for enum-compat ... done
  Stored in directory: /home/pi/.cache/pip/wheels/cb/f2/00/7616514d23c84bf58b7e9d034cdb7ff92f1b93c08b6a21ca8b
Successfully built pygatt enum-compat
Installing collected packages: enum34, enum-compat, pyserial, pygatt
Successfully installed enum-compat-0.0.2 enum34-1.1.6 pygatt-3.2.0 pyserial-3.4
pi@raspi:~ $ 
pi@raspi:~ $ pip install pybluez[ble]
Collecting pybluez[ble]
  Downloading PyBluez-0.22.zip (109kB)
    100% |████████████████████████████████| 112kB 809kB/s 
Collecting gattlib==0.20150805 (from pybluez[ble])
  Downloading gattlib-0.20150805.tar.gz (1.7MB)
    100% |████████████████████████████████| 1.7MB 143kB/s 
Building wheels for collected packages: pybluez, gattlib
  Running setup.py bdist_wheel for pybluez ... done
  Stored in directory: /home/pi/.cache/pip/wheels/e7/40/9d/b772a3cf2ca121e87a06eabe9483271816581dec7c772272d3
  Running setup.py bdist_wheel for gattlib ... done
  Stored in directory: /home/pi/.cache/pip/wheels/7d/15/79/77d35f4d5dbbf551c670ee1dc11fdb97a52c3445b8a5cbd96b
Successfully built pybluez gattlib
Installing collected packages: gattlib, pybluez
Successfully installed gattlib-0.20150805 pybluez-0.22
pi@raspi:~ $ 
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get install -y build-essential
Reading package lists... Done
Building dependency tree       
Reading state information... Done
build-essential is already the newest version (12.3).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
pi@raspi:~ $ 
pi@raspi:~ $ 
pi@raspi:~ $ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -

## Installing the NodeSource Node.js v6.x repo...


## Populating apt-get cache...

+ apt-get update
Hit:1 http://mirrordirector.raspbian.org/raspbian stretch InRelease
Hit:2 http://archive.raspberrypi.org/debian stretch InRelease
Reading package lists... Done

## Confirming "stretch" is supported...

+ curl -sLf -o /dev/null 'https://deb.nodesource.com/node_6.x/dists/stretch/Release'

## Adding the NodeSource signing key to your keyring...

+ curl -s https://deb.nodesource.com/gpgkey/nodesource.gpg.key | apt-key add -
OK

## Creating apt sources list file for the NodeSource Node.js v6.x repo...

+ echo 'deb https://deb.nodesource.com/node_6.x stretch main' > /etc/apt/sources.list.d/nodesource.list
+ echo 'deb-src https://deb.nodesource.com/node_6.x stretch main' >> /etc/apt/sources.list.d/nodesource.list

## Running `apt-get update` for you...

+ apt-get update
Hit:1 http://mirrordirector.raspbian.org/raspbian stretch InRelease
Hit:2 http://archive.raspberrypi.org/debian stretch InRelease
Get:3 https://deb.nodesource.com/node_6.x stretch InRelease [4,647 B]
Get:4 https://deb.nodesource.com/node_6.x stretch/main Sources [765 B]
Get:5 https://deb.nodesource.com/node_6.x stretch/main armhf Packages [1,009 B]
Fetched 6,421 B in 1s (3,607 B/s)    
Reading package lists... Done

## Run `apt-get install nodejs` (as root) to install Node.js v6.x and npm

pi@raspi:~ $ 
pi@raspi:~ $ ^Zsudo apt-get install -y nodejs^C
pi@raspi:~ $ 
pi@raspi:~ $ sudo apt-get install -y nodejs
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following package was automatically installed and is no longer required:
  libuv1
Use 'sudo apt autoremove' to remove it.
The following packages will be REMOVED:
  nodejs-legacy nodered
The following packages will be upgraded:
  nodejs
1 upgraded, 0 newly installed, 2 to remove and 0 not upgraded.
Need to get 8,780 kB of archives.
After this operation, 28.0 MB of additional disk space will be used.
Get:1 https://deb.nodesource.com/node_6.x stretch/main armhf nodejs armhf 6.12.0-1nodesource1 [8,780 kB]
Fetched 8,780 kB in 3s (2,428 kB/s)  
apt-listchanges: Reading changelogs...
(Reading database ... 136709 files and directories currently installed.)
Removing nodered (0.17.4) ...
Removing nodejs-legacy (4.8.2~dfsg-1) ...
(Reading database ... 129820 files and directories currently installed.)
Preparing to unpack .../nodejs_6.12.0-1nodesource1_armhf.deb ...
Unpacking nodejs (6.12.0-1nodesource1) over (4.8.2~dfsg-1) ...
Processing triggers for mime-support (3.60) ...
Processing triggers for desktop-file-utils (0.23-1) ...
Setting up nodejs (6.12.0-1nodesource1) ...
Processing triggers for gnome-icon-theme (3.12.0-2) ...
Processing triggers for man-db (2.7.6.1-2) ...
Processing triggers for gnome-menus (3.13.3-9) ...
pi@raspi:~ $ 
pi@raspi:~ $ 
pi@raspi:~ $ git clone https://github.com/mbientlab/MetaWear-SDK-JavaScript.git
Cloning into 'MetaWear-SDK-JavaScript'...
remote: Counting objects: 109, done.
remote: Total 109 (delta 0), reused 0 (delta 0), pack-reused 109
Receiving objects: 100% (109/109), 21.29 KiB | 0 bytes/s, done.
Resolving deltas: 100% (50/50), done.
pi@raspi:~ $ 
pi@raspi:~ $ ls
Desktop    Downloads                Music     Public        Templates
Documents  MetaWear-SDK-JavaScript  Pictures  python_games  Videos
pi@raspi:~ $ cd MetaWear-SDK-JavaScript/
pi@raspi:~/MetaWear-SDK-JavaScript $ ls
examples  index.js  Jenkinsfile  lib  LICENSE  MetaWear-SDK-Cpp  package.json  README.md  test
pi@raspi:~/MetaWear-SDK-JavaScript $ cd examples/
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ ls
anonymous_datasignals.js  connect.js  led.js  logging.js  multi_device.js
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ nano led.js 
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 

```

