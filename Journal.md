# Project Journal

**Project Name:** LoRa-Com  
**Start Date:** 05-09-2026  
**Status:** In Progress

## Overview
A communication device that lets you send text messages without using Wi-Fi, cellular service, or a SIM card. 

## Recent Entries

### 05-09-2026 - First Journal Entry

**How I got the idea:**
<br>
So yesterday I was chilling in the park. I was alone so I had the idea to call my friend and ask my friend if he could also come. I then tried to call him but then I got reminded that "Ohh I dont have the call balance to do so" which got me frustrated with the idea that you need Sim cards, wifi to send your desired message to your destination. Thats when my mind clicked an idea. "What if I could build a device that no longer needs any of that?". I came home and researched about the device and the first thing the showed up was a LoRa-Communicator and then I decided I really wanna build that.. and So I got into action

**What I did today:**
<br>
So I am gonna start by researching how a LoRa messenger device works cause i know shi.. about tht and then i'll be moving towards researching about the components that are required to build the device..
So the working is pretty simple..
<img width="665" height="144" alt="image" src="https://github.com/user-attachments/assets/30526f34-77ca-4fbc-aeb0-a8822864f129" />
<br>
So basically the MCU sned digital signals to the transceiver and its converts it into radio waves and the transceiver on the receiver side which has the same frequency picks those radio waves which are manipulated by their frequency and then demodulation happens to revert those waves..
<br>
Now I am gonna start researching about all the Components that are required to build the devive...
<br>

1- Microcontroller 
<br>
So the first component we need is an MCU or a microcontroller to convert data to digital signals..
<br>
2- LoRa radio module
<br>
The second thing we need is a LoRa radio module to send and receive radio signals using very less electricity..
<br>
3- Display (OLED OR E-PAPER)
<br>
Then we need a display to show the actual data or message which is being transmitted..
<br>
4- Input module 
<br>
The next thing is an keyboard module so that we can give the input to the device..
<br>
5- LiPo battery
<br>
And the fifth thing is the power supply for which we need a LiPo battery 3.7V
<br>
6- Charger Module
<br>
The next thing is a charger module with protection to charge out LiPo battery
<br>
7- Voltage regulator 
<br>
And a voltage regulator to maintain a stable 3.3V/5V rail.
<br>
8- LoRa Antenna (+ connector)
<br>
The next thing is gonna be antennas with connectors 
<br> 
9- USB connector
<br>
Then I would need a usb connecttor to for flash firmware etc
<br>
10- Power switch
<br>
Then a power switch which is a physical on/off switch (or soft-power circuit) so you I fully disconnect the battery.
<br>
11- Battery voltage monitoring
<br>
Now I need some sort of battery monitoring system. without this you cannot show battery percentage or implement low battery shutdown.
<br>
12- Basic passive components
<br>
Decoupling capacitors (0.1 µF + 10 µF near every IC), pull-up resistors (for I2C on the ATECC608A, BME sensor, keyboard expander, etc.), series resistors for LEDs/encoders, and possibly a 32.768 kHz crystal for accurate RTC


Now that I am gone with the necessary components, I am gonna start putting some extra cool things in my device too.. Lets research about what are the cool things I can add..

<br>
1- Rotary Encoder 
<br>
The first thing I wanna add will be a Rotary encoder to scroll thro options...
<br>
2- GNSS/GPS Modules
<br>
The Second I am gonna add would be GNSS/GPS Modules to calculate device's physical coordinates such as latitude longitude and altitude using signals from global navigation satellites.
<br>
3- BME280 / BME680 Sensors
<br>
The next Thing I really wanna add and I think that would be soo cool to add is gonna be Sensors to Measure temperature humidity pressure and indoor air quality (gas tracking) to build a remote weather station.
<br>
4- ATECC608A
<br>
Last but not the Least, The final thing I am gonna add would be a ATECC608A to secure data at the hardware level. It adds military-grade encryption keys to LoRaWAN packets.


