# self-watering
A project to create a self watering system for plants

## Goal

Ok I would like to say I travel a lot or something like that, but I just forget to water my plants.

So like any lazy engineer I want to create an automatic watering system.  But not just any system.
I want it to use minimal water, I want it te be self-contained and I want it to be solar-powered.

I created versions 1, 2 and 3 with an off the shelf set of electronic bough online, but I have found 
them lacking.  

This project will be my attempt to create a better self watering system.

This was what I used for versions 1 & 2.  https://www.amazon.com/Diitao-Automatic-Irrigation-Capacitive-Detection/dp/B0B7LMFRKS

For version 3 I replaced the pump with one that a can place outside the water storage tank.

While it somewhat works, I think we can do better.

To that end ths is what my research to date has shown.

First, the solar panel is great and provides plenty of power at full sun.  But while the sun is rising
and setting, or if there are clouds, it can cause the system to stutter.  That is it has enough power 
to start then when the motor starts, it draws the voltage too low and shutdowns, only to restart as soon 
as its shutdown.

So we need a first stage circuit that will only start at some high voltage and will shut down when the voltage 
drops below some minimum voltage and will only restart once the hgh voltage is available again.  Ideally a resistor 
to set the both the low and high voltages so we can "play" with it to get the best setting.

Searching found this:  https://electronics.stackexchange.com/questions/661213/low-voltage-cut-off-of-solar-panel-supply

Second, the kit I bought used a relay.  While it works, being outdoors exposed to moisture it is only a matter of time
before the contacts corrode.

So for the second stage moisture sensing circuit, we need to replace the relay with a MOSFET to control the motor. 

Finally, if something goes wrong, there is no way to know until the plant start dying.  So I would like 
a second version of the moisture sensor circuit with a buzzer and led so we can set it to slightly less moisture 
than the one that drives the motor.  This circuit will drive a buzzer and led so we know something is wrong,
the buzzer tells us something is wrong, and led helps us find the one that is buzzing.

Key part ideas:

Short circuit protection: https://www.mouser.com/ProductDetail/YAGEO/BK60-005-DZ?qs=PzGy0jfpSMvFI562sjyP8A%3D%3D

The good old LM393: https://www.ti.com/product/LM393

Possible MOSFET: https://www.mouser.com/ProductDetail/onsemi-Fairchild/FDC642P

Parts I am using so far:

Solar panels:

https://www.aliexpress.com/item/3256806980290613.html

https://www.amazon.com/dp/B0D86YFRF3

Pump:

https://www.aliexpress.com/item/3256804920163520.html

Soil probe: 

https://www.aliexpress.com/item/3256806726279754.html

