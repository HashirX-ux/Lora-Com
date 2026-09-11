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
12- Status LEDs
<br>
Status LEDs are important to show the status if Power, charging, TX/RX 
<br>
13- Reset button
<br>
Hardware reset is almost always needed to reset the internal hardware for flasg etc
14- Basic passive components
<br>
Decoupling capacitors (0.1 µF + 10 µF near every IC), pull-up resistors (for I2C on the ATECC608A, BME sensor, keyboard expander, etc.), series resistors for LEDs/encoders, and possibly a 32.768 kHz crystal for accurate RTC
<br>
15- GPS Antenna
<br>
Most GNSS modules perform much better (or only work properly) with a dedicated antenna

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
<br>
5- Buzzer or Vibration motor
<br>
So Its gonna act as a Notification feedback when a message arrives and the buzzer gonna make the sound to indicate..
<br>
<br>

So Now I am done researching all the components that I am gonna use for my LoRa device. Now i am gonna start researching about each component indivudually so that I can understand datasheets of the components..
<br>
Lets start by Microcontroller... So the first MCU I have found That I can Use in my device is Nordic nrf52840. This MCU mainly supports sustainable battery power and a long lasting battery and also features mobile phone connection via bluetooth. 

<img width="832" height="329" alt="image" src="https://github.com/user-attachments/assets/3d49604c-2ad5-478f-bccb-4f9c60abc88f" />
<br>

It does looks cool 
<br>
<img width="756" height="291" alt="image" src="https://github.com/user-attachments/assets/e6c6a063-40e8-45e2-85e4-b86e6631d421" />
<br>

My Preference is that I wanna use such MCU that provides a cool looking UI for the user cuz yk it gives more of that hacker asthetic vibe.. For that purpose that Best MCU I have found is ESP32-S3 according to my research

<img width="792" height="97" alt="image" src="https://github.com/user-attachments/assets/1f0c9f5f-7e9a-42ed-b99a-bd6c47004e25" />
<br>

This is how a ESP32-S3 Looks: 
<br>
<img width="1262" height="613" alt="image" src="https://github.com/user-attachments/assets/bb219c4b-2615-4f32-a12a-f9f03fd5fc5c" />
<br>

Since I am preferring to use a cool looking User interface for my LoRa Device like the one that gives yk that hacker asthetic vibe, SO I am gonna be using the one and only ESP32-S3 as my MCY for my LoRa Device 
- MCU --> ESP32-S3

Now I am gonna start researching about How an ESP32-S3 board actually works by reading the datasheets and the pinouts and what are their functions..SO basically its an MCU based system on chip device (SoC) which means it has all the components of a computer or an electronic system.. I rly have no idea how the heck did they even fit those tiny components in that chip..

<img width="935" height="742" alt="image" src="https://github.com/user-attachments/assets/43129db9-b670-4a2e-86a6-2b39e06f7f1b" />

Obviously My dumb ahh brain has no idea what even is this diagram cause its the first time I am using this kind of Microcontroller 
<img width="1154" height="710" alt="image" src="https://github.com/user-attachments/assets/bade647e-1101-4296-8418-44f6fbfa34d3" />
<br>
So the ESP32-S3 has 45 general purpose pins meaning these pins can be used to connect external devices in order to communicate with the MCU
<img width="704" height="731" alt="image" src="https://github.com/user-attachments/assets/840913a3-d273-47ca-a53f-fd2ef85dcc74" />
<br>
Yeah I am definatly gonna add GNSS system to my LoRa device.. This is gonna look so damn cool...
<img width="791" height="114" alt="image" src="https://github.com/user-attachments/assets/633aa2e9-6481-4847-8262-e6f7f856bd5b" />
<br>
Overall There are three types of pins in the esp32-s3. 
- Analog Pins
- Power pins
- GPIO pins
<br>
The first one is the Analog pins to measure continuous analog signals like temperature etc. The second type of pins are the power pins that provide 5v and 3.3V power supply based on your usage. I can use 5V pin to power the USB-C device and 3.3V to power the Small sensors or displays to show data and then there are GPIO pins to connect external components..
<br>
<img width="401" height="701" alt="image" src="https://github.com/user-attachments/assets/7f068208-16e0-46a9-83ea-b8f68bf41a39" />
<br>
Didnt knew that a single pin could handle multiple input/output signals. I wonder how does that even work in the first place
<img width="1225" height="129" alt="image" src="https://github.com/user-attachments/assets/07195dd4-a9d9-49a4-b441-ddce8a6340a9" />
<br>

Ok I guess its enough about the MCU, Ill continue the research on the ESP32-S3 when in need again So Now I am gonna start about the LoRa radio module and how can i use that stuuff in my schematic..
<br>
So SX1262 is considered one of the best radio nodules to use for the LoRa Messenger
<img width="827" height="112" alt="image" src="https://github.com/user-attachments/assets/66b588bd-7587-4399-8245-dd8ba291bbfb" />
<br>

So this is how the best LoRa Radio module looks like which are SX1262 based modules
<br>
<img width="265" height="280" alt="image" src="https://github.com/user-attachments/assets/376744b1-5768-4d3e-a0fd-b13338e57233" />
<br>
I basically have no I idea what is the meaning of these features but ts frr looks cool to use as a LoRa radio module..
<img width="450" height="321" alt="image" src="https://github.com/user-attachments/assets/8ec00866-bd30-4320-b87f-1da2681a65fc" />
<br>
No that I am done with the LoRa radio module setup and datasheet, Ill be moving towards the display that I am gonna use. I have researched about the best display to use and I am getting a small OLED display (like the SSD1306 128x64 pixels) which is generally the best choice for a basic, low-power LoRa messenger.
<br>
<img width="809" height="103" alt="image" src="https://github.com/user-attachments/assets/33efcd91-dc94-40bc-9494-2254960b6705" />

For Display I am choosing Waveshare 3.5" IPS capacitive touchscreen. This screen has a touch screen allowing the user to cimmunicate thro the screen to
<br>
<img width="714" height="528" alt="image" src="https://github.com/user-attachments/assets/b6229069-cb50-480a-aefe-22b9769808df" />

Now for the keyboard I am gonna use the built in KiCad sw-push switches that are gonna help alot 
<img width="784" height="651" alt="image" src="https://github.com/user-attachments/assets/1ac5db90-9232-4202-b7c8-ef7a066c9201" />
<br>
The battery is gonna be LiPo 3.7V which is kinda ugly to use but its ok and also I am gonna use TP4056 Module as charger and protection module 
<br>
<img width="378" height="321" alt="image" src="https://github.com/user-attachments/assets/7e7682ac-1b58-4da8-91e1-4964fdac8527" />
<img width="855" height="625" alt="image" src="https://github.com/user-attachments/assets/4c7f2bce-6a97-4d66-9e0f-b6b8e7507bf5" />

The Voltage regulator that I am gonna use is gonna be AP2112K-3.3
<br>
<img width="397" height="408" alt="image" src="https://github.com/user-attachments/assets/6b79598d-0c3c-4e7e-8fa0-fda90872712e" />

For the USB connector I am gonna use USB-C to connect the device and so its gonna also be rechargable
<img width="694" height="497" alt="image" src="https://github.com/user-attachments/assets/46a24ebb-6036-43e8-986e-8af0a41650f5" />
<br>

For Real time sattelite data I am gonna be using MAX-M8Q
<br>
<img width="372" height="386" alt="image" src="https://github.com/user-attachments/assets/a49ec1df-f6c8-4194-9136-51d72a1dba3e" />

For rotary Encoder I am gonna be using EC11 standard rotary encoder.
<br>
<img width="378" height="359" alt="image" src="https://github.com/user-attachments/assets/9eadd733-3c6d-4535-a5ba-b38e577e2ba8" />

Now I am gonna research about BME680 to measure temperature, humidity, barometric pressure, and volatile organic compounds (VOCs) for indoor air quality assessment.
<br>
<img width="410" height="393" alt="image" src="https://github.com/user-attachments/assets/6425c56e-9d07-4af5-b991-77d499f0918c" />

No I am gonna add the ATECC608A which is a secure element and cryptographic co-processor from Microchip Technology designed to provide hardware-based security, secure key storage, and cryptographic acceleration for embedded systems and Internet of Things (IoT) devices
<img width="559" height="475" alt="image" src="https://github.com/user-attachments/assets/6645ef6d-dfe3-4a6d-ba2f-68b9b36d2d81" />

Now I am gonna start working schematic. For making the schematic I am gonna use KiCad 
<img width="779" height="678" alt="image" src="https://github.com/user-attachments/assets/04bec1e6-b8a4-4f10-a02b-bbc6602f2435" />

This is the order for me to build the schematic for my LoRa device keyboard
<img width="779" height="520" alt="image" src="https://github.com/user-attachments/assets/71a882e1-a20e-4cf2-aa89-0e8772c9e316" />








