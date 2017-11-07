# notes

Mike is having trouble with the mbient labs MetaHub tutorial.  
tl;dr the problem appears to be with the `bindings` file.  It might be related to [a note](https://github.com/mbientlab/MetaWear-SDK-Cpp/commit/3906944af4e78bd86a8ac5f4ba01a7ca42ce4451) that [scaryghost](https://github.com/scaryghost) referred to in a [commit comment](https://github.com/mbientlab/MetaWear-SDK-Cpp/tree/master/bindings): "Forgot to commit updated JS bindings".   


---

I followed the [MetaHub tutorial](https://mbientlab.com/tutorials/MetaHub.html) and cloned the [JavaScript repo](https://github.com/mbientlab/MetaCloud-SDK-JavaScript). _The only steps that I skipped was [21.1](https://mbientlab.com/tutorials/MetaHub.html#setup-your-hub) since I used the GUI rather than CLI._ I did everything from [21.4.3](https://mbientlab.com/tutorials/MetaHub.html#build-your-own-hub) through the end. In case it matters, I installed `setup_6.x` and not `setup_8.x`. Now I'm getting a `debug` error (below). You can see the [linux details here](https://github.com/mikimer/notes/blob/master/details.md) and a [photo of my setup](https://github.com/mikimer/notes/blob/master/IMG_1393.JPG).

-------

It's now 1.30pm (I emailed Laura at 12noon), I'm still trying to get the MetaHub to work.
I noticed that in the [JavaScript Github README](https://github.com/mbientlab/MetaWear-SDK-JavaScript) it says to run `npm install metawear`, but when I do that my [RPi freezes](https://github.com/mikimer/notes/blob/master/IMG_1530.JPG) :(

-----

It's now 2pm. I missed some of the subtleties of the instructions. I added the noble packages. Now I've got progress and new problems :)
https://github.com/mikimer/notes/blob/master/details2.md 

```
pi@raspi:~/MetaWear-SDK-JavaScript/examples $ 
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

```

----

It's now 3pm  
I'm going to try to use Python instead of JavaScript...  
I'm getting another error related to `cbindings`  
Details here: https://github.com/mikimer/notes/blob/master/details3.md  
