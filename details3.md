
It's 3pm. I'm trying to use Python instead of JavaScript and RPi still isn't working as a MetaHub.  
I'm getting another error referring to `cbindings`.

```
pi@raspi:~/MetaWear-SDK-Python $ ls
examples  LICENSE.txt  MANIFEST.in  mbientlab  MetaWear-SDK-Cpp  README.rst  setup.py  test.py
pi@raspi:~/MetaWear-SDK-Python $ 
pi@raspi:~/MetaWear-SDK-Python $ py setup.py 
bash: py: command not found
pi@raspi:~/MetaWear-SDK-Python $ 
pi@raspi:~/MetaWear-SDK-Python $ python test.py 
Traceback (most recent call last):
  File "test.py", line 1, in <module>
    from mbientlab.metawear import MetaWear, libmetawear, parse_value
  File "/home/pi/MetaWear-SDK-Python/mbientlab/metawear/__init__.py", line 5, in <module>
    from .cbindings import *
ImportError: No module named cbindings

PS> Also I don't know much about Python. Maybe it looks like bad Python installation. Maybe wrong Python version? 2 vs 3

pi@raspi:~/MetaWear-SDK-Python $ 
pi@raspi:~/MetaWear-SDK-Python $ cd examples/
pi@raspi:~/MetaWear-SDK-Python/examples $ 
pi@raspi:~/MetaWear-SDK-Python/examples $ ls
anonymous_datasignals.py  led.py  multi_device.py  scan_connect.py
pi@raspi:~/MetaWear-SDK-Python/examples $ python led.py 
Traceback (most recent call last):
  File "led.py", line 9, in <module>
    device = MetaWear(sys.argv[1])
IndexError: list index out of range
pi@raspi:~/MetaWear-SDK-Python/examples $ 
pi@raspi:~/MetaWear-SDK-Python/examples $ 
pi@raspi:~/MetaWear-SDK-Python/examples $ python scan_connect.py 
Traceback (most recent call last):
  File "scan_connect.py", line 14, in <module>
    devices = service.discover(2)
RuntimeError: Set scan parameters failed (are you root?)
pi@raspi:~/MetaWear-SDK-Python/examples $ 
pi@raspi:~/MetaWear-SDK-Python/examples $ 
pi@raspi:~/MetaWear-SDK-Python/examples $ sudo python scan_connect.py 
Traceback (most recent call last):
  File "scan_connect.py", line 2, in <module>
    from mbientlab.metawear import MetaWear
ImportError: No module named mbientlab.metawear

PS> Looks like bad install indeed...

pi@raspi:~/MetaWear-SDK-Python/examples $ 

```
