# Notes with Bryan Reed
-- EDM Attentuation control was not set up

Things that go wrong:
windows drivers reassign com port numbers
In settings-> check the COM port. Currently, it is COM3. In windows device manager, you can see what disappears when you unplug the signal combiner. 


Button connects to the IDES Attenuation Control Software. 

If there is a charging problem, it is due to something between the driver and the plates. 
The driver produces a voltage of 100V to the plates. The black box has a programmable power supply and a switch. 
Signal combiner is powered over usb and produce 3.5V TTL to tell the power supply when to blank. 
Slow mode can enable longer dwell times


Synchrony software : 1.3.7. This can be updated. The light weight rest server/driver which spits out current info at 43376 localhost. 
if you go to localhost:43376\DosePainter/ --> you can access dosepainter info. 

Synchrony software was never set up!

# Hardware
Top one is synchrony. Bottom is EDM.
In synchrony box, there is an FPGA and ARM motherboard. The firmware is in an SD card instead of on ROM. 
Boot.bin is the firmware-- this can be modified easily. 
The config.json file has an IP address of 172.17.41.12 which corresponds to the Synchrony FPGA. 

The knob on the table produces PWM without sync with the beam. 
The Synchrony Dose Painter Global Dose Modulator is synced with the beam scan. 

# Synchrony dose painter software:
Initialize dose painter. 
Then you see a Proceed to Dose Painter button on the home page. 
DPG (Digital Pattern Generator, which is basically the box for the FPGA) Options -> 172.17.41.12

You can select FEMTUS(MDP) or AIP 

When we change the dwell time, the image shifts-- this is a scanning calibration which needs to be fixed. 

If you paint shapes and the press execute mask-- you will see the dose change in FEMTUS. 
Blank when stopped and combo of enable inps synchrony can create behavior I dont understand. 

- The acquire button did not work on Synchrony dose painter, although the free run works. Acquire does not acquire in FEMTUS, but it acquires in Dose Painter. Acquire Automation through FEMTUS REST Interface is not working. 

EDS should also work with dose painter, but the GMS scan generator is not configured to work with synchrony. 
# Tempo 
