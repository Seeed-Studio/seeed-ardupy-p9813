# Seeed ArduPy P9813 [![Build Status](https://api.travis-ci.com/Seeed-Studio/seeed-ardupy-p9813.svg?branch=master)](https://travis-ci.com/github/Seeed-Studio/seeed-ardupy-p9813)

## Introduction

Grove - Chainable RGB LED is based on P9813 chip which is a full-color LED driver. It provides 3 constant-current drivers as well as modulated output of 256 shades of gray. It communicates with a MCU using 2-wire transmission (Data and Clock). This 2-wire transmission can be used to cascade additional Grove - Chainable RGB LED modules. The built-in clock regeneration enhances the transmission distance. This Grove module is suitable for any colorful LED based projects.

You can get more information in here [Grove_Chainable_RGB_LED](https://github.com/Seeed-Studio/Grove_Chainable_RGB_LED).


<img src=https://statics3.seeedstudio.com/images/product/chanbalelednb1.jpg width=300><img src=https://statics3.seeedstudio.com/product/chanbalelednb1_02.jpg width=300>

[Grove – Chainable RGB Led V2.0](https://www.seeedstudio.com/Grove-%E2%80%93-Chainable-RGB-Led-V2.0-p-2903.html)

<img src=https://statics3.seeedstudio.com/seeed/file/2017-07/bazaar501790_10402004845.jpg width=300><img src=https://statics3.seeedstudio.com/seeed/file/2017-07/bazaar501794_1040200484.jpg width=300>


## How to binding with ArduPy
- Install [AIP](https://github.com/Seeed-Studio/ardupy-aip)
- Build firmware with Seeed ArduPy P9813
```
    aip install Seeed-Studio/seeed-ardupy-p9813
    aip build
```
- Flash new firmware to you ArduPy board
```
    aip flash <path of the new firmware>
```
For more examples of using AIP, please refer to [AIP](https://github.com/Seeed-Studio/ardupy-aip).

## Usage

```
from arduino import grove_chainable_led
import time

rgb_led = grove_chainable_led(0, 1, 1) #clock, data, led_numbers

while True:
    rgb_led.set_rgb(1, 255, 0, 0) #NO, red, green, blue
    time.sleep(2)
    rgb_led.set_rgb(1, 0, 255, 0)
    time.sleep(2)
    rgb_led.set_rgb(1, 0, 0, 255)
    time.sleep(2)
    rgb_led.set_rgb(1, 0, 255, 255)
    time.sleep(2)
    rgb_led.set_rgb(1, 255, 0, 255)
    time.sleep(2)
    rgb_led.set_rgb(1, 255, 255, 0)
    time.sleep(2)
    rgb_led.set_rgb(1, 255, 255, 255)
    time.sleep(2)
```

## API Reference

- **set_rgb(*No, R, G, B*)**

    Set RGB corresponding to LED No.
    ```
    rgb_led.set_rgb(1, 255, 0, 0) # Make LED No. 1 red
    ```

- **set_hsb(*No, H, S, B*)**

    Set HSB corresponding to LED No.
    ```
    rgb_led.set_rgb(1, 0.025, 1.0, 0.5)
    ```

----

This software is written by seeed studio<br>
and is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt for more information.<br>

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>