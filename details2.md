
Progress!  I figured out that I did the `git clone` on the JavaScript repo, but I didn't follow all the steps in the [**Instructions**](https://github.com/mbientlab/MetaWear-SDK-JavaScript#install).

Now I've got a new error going:

```pi@raspi:~/MetaWear-SDK-JavaScript $ 
pi@raspi:~/MetaWear-SDK-JavaScript $ sudo apt-get install bluetooth bluez libbluetooth-dev libudev-dev
Reading package lists... Done
Building dependency tree       
Reading state information... Done
bluez is already the newest version (5.43-2+rpt2+deb9u2).
bluez set to manually installed.
libbluetooth-dev is already the newest version (5.43-2+rpt2+deb9u2).
The following package was automatically installed and is no longer required:
  libuv1
Use 'sudo apt autoremove' to remove it.
Suggested packages:
  bluez-cups bluez-obexd
The following NEW packages will be installed:
  bluetooth libudev-dev
0 upgraded, 2 newly installed, 0 to remove and 0 not upgraded.
Need to get 132 kB of archives.
After this operation, 251 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.raspberrypi.org/debian stretch/main armhf bluetooth all 5.43-2+rpt2+deb9u2 [41.5 kB]
Get:2 http://mirrordirector.raspbian.org/raspbian stretch/main armhf libudev-dev armhf 232-25+deb9u1 [90.6 kB]
Fetched 132 kB in 0s (165 kB/s)                                          
Selecting previously unselected package libudev-dev:armhf.
(Reading database ... 132754 files and directories currently installed.)
Preparing to unpack .../libudev-dev_232-25+deb9u1_armhf.deb ...
Unpacking libudev-dev:armhf (232-25+deb9u1) ...
Selecting previously unselected package bluetooth.
Preparing to unpack .../bluetooth_5.43-2+rpt2+deb9u2_all.deb ...
Unpacking bluetooth (5.43-2+rpt2+deb9u2) ...
Setting up bluetooth (5.43-2+rpt2+deb9u2) ...
Processing triggers for man-db (2.7.6.1-2) ...
Setting up libudev-dev:armhf (232-25+deb9u1) ...
pi@raspi:~/MetaWear-SDK-JavaScript $ 
pi@raspi:~/MetaWear-SDK-JavaScript $ 
pi@raspi:~/MetaWear-SDK-JavaScript $ npm install noble
metawear@0.1.0 /home/pi/MetaWear-SDK-JavaScript
└── noble@1.8.1 

npm WARN optional SKIPPING OPTIONAL DEPENDENCY: xpc-connection@~0.1.4 (node_modules/noble/node_modules/xpc-connection):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for xpc-connection@0.1.4: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"arm"})
npm WARN optional SKIPPING OPTIONAL DEPENDENCY: xpc-connection@~0.1.4 (node_modules/metawear/node_modules/noble-device/node_modules/noble/node_modules/xpc-connection):
npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for xpc-connection@0.1.4: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"arm"})
pi@raspi:~/MetaWear-SDK-JavaScript $ 
pi@raspi:~/MetaWear-SDK-JavaScript $ ls
examples  Jenkinsfile  LICENSE           node_modules  README.md
index.js  lib          MetaWear-SDK-Cpp  package.json  test
pi@raspi:~/MetaWear-SDK-JavaScript $ cd examples/
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ ls
anonymous_datasignals.js  connect.js  led.js  logging.js  multi_device.js
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ node led.js 
module.js:471
    throw err;
    ^

Error: Cannot find module '../MetaWear-SDK-Cpp/bindings/javascript/cbindings'
    at Function.Module._resolveFilename (module.js:469:15)
    at Function.Module._load (module.js:417:25)
    at Module.require (module.js:497:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/home/pi/MetaWear-SDK-JavaScript/lib/metawear.js:17:17)
    at Module._compile (module.js:570:32)
    at Object.Module._extensions..js (module.js:579:10)
    at Module.load (module.js:487:32)
    at tryModuleLoad (module.js:446:12)
    at Function.Module._load (module.js:438:3)
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 


```
