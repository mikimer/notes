# notes

Mike is having trouble with the mbient labs MetaHub tutorial.

I followed all of the instructions here: https://mbientlab.com/tutorials/MetaHub.html

I'm getting a `debug` error (below). You can see the full details [here](https://github.com/mikimer/notes/blob/master/details.md).

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

