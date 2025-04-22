# Requirements for PCB

## Basic version 1.0

For the most basic version 1.0, we want a self-assembled kit that can be put together by the
novice.  This version should use though hole assembly and parts if possible.

All connectors should use though hole headers such as https://www.digikey.com/en/products/detail/w-rth-elektronik/61301611121/4846854.

Power, motor and LED connectors should be keyed like https://www.sparkfun.com/polarized-connectors-header-2-pin.htm

The buzzer is off the board and is something like https://www.digikey.com/en/products/detail/soberton-inc/PT-1303T/16354860

Water sensor probe and buzzer connector need not be keyed, but can be.

Where possible, though-hole components should be used so the novice soldering iron user can assemble it.


### Power 

The power should only be turned on after the voltage reaches some threshold to be determined by 
a variable restore. For basic version 1.0 the expected power is about 5 volts.  We will have a need for a 12 volt 
version as well, but version 1.0 will only be available in 5 volts.

The power shoud have a keyed header for a LED so we know when power is available.

We will test power on/off by using a dark piece of paper and sliding it across the solar panel until the 
circuit turn off.  Then we will uncover the panel until the circuit turns on. We will do this both under load
and with just the alarm circuit active.  This is to simulate the sun rising, setting and being covered by clouds.

The circuit is a success when it can be set to not cycle quickly under partial cover, but turns on and off
without stuttering.

### Moisture sensor turns pump on/off

The pump power should only turn on when the water probe lacks sufficient moisture.  

The set point for where the pump turns on should be set by an onboard variable resister. 

The motor sensor should have a keyed header for a LED so we know when the pump should be running.

We will test the moisture sensor by putting it in dry soil.  It should turn on the pump.  We will then 
add water to the soil until the pump turns off. 

The circuit is a success when it turns on the pump to water the soil then turns off the pump based on
where the variable resistor is set.

### Moisture alarm turns on/off

The alarm should only turn on when the water probe lacks sufficient moisture.  This setting should be 
independent of the pump moisture sensor.

The set point for where the moisture alarm turns on should be set by on onboard variable resister.

There should be two headers for the moisture alarm, one for a LED and one for a buzzer.

We will test the moisture sensor just like the pump on/off test.

The circuit is a success when the alarm turns on when the soil is too dry.

## Other versions 

### PCBWay assembled version

This version is optimized for automated assembly and uses surface mount parts rather than though hole so we
can get them assembled by PCBWay.

### 12 volt version

This version is just like the 5 volt version but runs on 12 volts and supports a 12 volt pump for larger 
watering projects.

This version should be surface mount for assembly by PCBWay.

### (Optional) Battery charge version

This version includes a circuit to charge an extern battery.  The Connector should be keyed.

