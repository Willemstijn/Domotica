# Adding Z-wave devices
## Adding a Z-Wave device in Domoticz.

De onderstaande procedure werkt bij het toevoegen van een nieuw ZWave device:
* Reset het device eerst door 10 sec op het 'pairing' knopje te drukken. Leds gaan dan lang knipperen.
* Na de reset open je Domoticz.
* Ga naar ``Setup > Hardware > Setup OpenZWave USB > Node management > Include node``
* Op het device: klik drie keer snel op de pairing button. Led gaat 5x snel knipperen.
* Domoticz zal (als het device binnen range is) de device detecteren en opnemen in de configuratie.
* Opnemen als device in het dashboard gaat via ``Setup > devices > Filter op 'Not Used'``
* Laat het device een alarm genereren. Refresh de pagina daarna.
* Als alles goed gaat staat het alarm van het device bovenaan. 
* Klik op het groene pijltje (wijst naar rechts), links naast 'Last seen'
* Geef het een betekenisvolle naam (PIR keuken)
* Nu is het device opgenomen in de lijst en kunnen er alarms of scripts mee gemaakt worden.

1. Go to 'Setup > Hardware > Select OpenZWave USB > Setup'.
2. Click right above the screen on the button 'Node Management', select 'Include Node'.
3. On the new ZWave device, click the pairing code on the pairing button (e.g. on the water detection device I had to press three times on the small black button left of the red LED).
4. Wait a moment and the device should be paired after a couple of seconds. [Adding sensor 2](./images/Zwave-watersensor-add-2.png) [Adding sensor 1](./images/Zwave-watersensor-add-3.png)
5. It will appear in the list of configured ZWave devices for further configuration.

## Adding the ZWave device to 

1. Go to 'Setup > Devices' and filter or browse through the list of detected devives.
2. CLick the small green arrow on the right side and give the device a meaningfull name. [Selection](./images/Select-watersensor.png)
3. Determine if the device is a main device or slave device. [MainDevice](./images/Watersensor-master.png)
4. Search for the new device under switches, temperature or Utility.
5. There you can configure the device further (icon, alarm type etc.) [Iconsettings](./images/Waterdetectie-Iconsettings.png)
6. Second you should determine if and how you are warned if the device detects an anomaly. [Alarmsettings](./images/Waterdetector-Alarmsettings.png)

## Configuring a ZWave device

1. Go to 'Setup > Hardware > Select OpenZWave USB > Setup'.
2. Select the device you want to configure.
3. Scroll down the page and click the button 'Request current stored values from device'.
4. Wait a minute and click the device again to see the current values (if correct, below the configuration the last update status should be a few minutes ago). [Configure sensor](./images/Zwave-watersensor-add-1.png)
5. Configure the device to your preferences and click the button 'Apply configuration for this device'.
6. Your now ready.

## Adding Devices

### Add a Neo coolcam Z-wave door sensor
The contact sensor can be included to the Z-wave network by pressing the code button. 

1. Disassemble  the  contact  sensor  main  body  and  insert  the  battery  into  the  contactsensor. Make sure the device is located within the direct range of the controller.
2. Set the controller into the learning mode (see mail controller’s operating manual).
3. Quickly, triple click the code button, LED light will flash for 5 times.
4. Contact sensor will be detected and included in the Z-Wave network.
5. Wait for the main controller to configure the sensor.

Excluding Sensor (contact senor) from Z-Wave Network 

1. Make sure the sensor is connected to power source.
2. Set  the  main  controller  into  the  learning  mode  (see  main  controller’s  operatingmanual). 
3. Quickly, triple click the code button,LED light will flash for 5 times.
4. Wait for the main controller to delete the sensor

More information is available in the [instruction manual](docs/neo_coolcam_door_window_sensor_user_manual.pdf).

### Add a Neo coolcam PIR
The PIR can be included to the Z-wave network by pressing on the code button.

1. Disassemble the PIR main body and insert the battery into the contact sensor. Make sure the device is located within the direct range of the controller.
2. Set the controller into the learning mode (see mail controller’s operating manual).
3. Quickly, triple click the code button, LED light will flash red for 5 times.
4. PIT will be detected and included in the Z-Wave network.
5. Wait for the main controller to configure the PIR.

Excluding Sensor (PIR) from Z-Wave Network

1. Make sure the sensor is connected to power source.
2. Set the main controller into the learning mode (see main controller’s operating manual).
3. Quickly, triple click the code button, LED light will flash red for 5 times.
4. Wait for the main controller to delete the sensor.

More information is available in the [instruction manual](docs/Manual-for-Motion-sensor-PIR-Zwave-Neo.pdf).

**Addemdum for Neo Coolcam devices**
For adding a Coolcam device I had to do the following trick to detect the devices:

* Reset the device to it's facory default by pressing the device button and holding it for 20 seconds.
* Remove battery and startup device
* Wait 10 seconds
* Go to "Setup > Devices > Setup OpenZwave USB > Node Management > Include node"
* Click the pairing/reset button 3 times quickly - the led should flash 5 times
* After a small time the device is added to Domoticz
* Remember the device NodeID (e.g. 0x12)
* Go to "Setup > Devices", filter on "Not used" and the NodeID [Image](images/2019-11-06-14-43-39.png)
* There will be multiple devices available, not all of them work as a sensor, except for the "Sensor" type for door sensors
* In case of PIR, you should select the "PIR sensor"
* Click on the green arrow right and give the device a name. 
* For testing purposes, you can make a device from each detected device and test which one will work. [imaeg](images/2019-11-06-14-45-45.png)
