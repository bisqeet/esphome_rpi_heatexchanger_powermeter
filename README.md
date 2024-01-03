# esphome_rpi_heatexchanger_powermeter
Using the s0 interface of the eltako 3-phase powermeter to integrate into home assistant via esphome using a raspberry pi pico

We recently swapped out an old diesel heating system and replaced it with a daikin heatexchanger (another project)
Unfortunately the integrated powermeter function for the daikin is broken, the values coming out of there are...not very useful.
Instead, i decided to integrate a seperate powermeter. This was easy (for me) to do as i installed a seperate switching cabinet for the power meter (ok, there was no room in the old one, so i had too)

![7FFE52A6-0DAE-4F1F-A94C-9B38DC63E245_1_105_c](https://github.com/bisqeet/esphome_rpi_heatexchanger_powermeter/assets/89842144/f0da6aff-68cf-4184-a3dc-8458206b7080)

![F04BB82E-B887-440F-AEED-186E276DEED4_1_105_c](https://github.com/bisqeet/esphome_rpi_heatexchanger_powermeter/assets/89842144/6a019a64-3531-4971-be01-b324bae5891e)

The 3 phase safety switch used is an eltako dz15d-3x80A (https://www.eltako.com/fileadmin/downloads/de/_bedienung/DSZ15D-3x80A_28380015-1_dt.pdf)
It has a potential free s0 interface (5v-30V) that pulses 1000 times per kilowatt (pulse length 30ms). 

As the GPIO pins are not 5V tolerant, I added a voltage divider to the input signal (top in fritzing).

I added an 1.2" breakout OLED (128x128) to display some stuff

![82DC8214-BE57-4007-949C-F2D527C4FBAC](https://github.com/bisqeet/esphome_rpi_heatexchanger_powermeter/assets/89842144/5e9e797a-0402-45a7-af84-e69e76556053)
