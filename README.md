# notes

Mike is having trouble with the mbient labs MetaHub tutorial.

I followed the [MetaHub tutorial](https://mbientlab.com/tutorials/MetaHub.html) and cloned the [JavaScript repo](https://github.com/mbientlab/MetaCloud-SDK-JavaScript). _The only steps that I skipped was [21.1](https://mbientlab.com/tutorials/MetaHub.html#setup-your-hub) since I used the GUI rather than CLI._ I did everything from [21.4.3](https://mbientlab.com/tutorials/MetaHub.html#build-your-own-hub) through the end. In case it matters, I installed `setup_6.x` and not `setup_8.x`. Now I'm getting a `debug` error (below). You can see the [linux details here](https://github.com/mikimer/notes/blob/master/details.md) and a [photo of my setup](https://github.com/mikimer/notes/blob/master/IMG_1393.JPG).

```
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ node led.js 
module.js:471
    throw err;
    ^

Error: Cannot find module 'debug'
    at Function.Module._resolveFilename (module.js:469:15)
    at Function.Module._load (module.js:417:25)
    at Module.require (module.js:497:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/home/pi/MetaWear-SDK-JavaScript/lib/metawear.js:4:29)
    at Module._compile (module.js:570:32)
    at Object.Module._extensions..js (module.js:579:10)
    at Module.load (module.js:487:32)
    at tryModuleLoad (module.js:446:12)
    at Function.Module._load (module.js:438:3)
```

