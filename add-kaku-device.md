# Adding a KAKU device to Domoticz

The RF devices that are supported by the RFXtrx433E are typically either devices that "transmit" or devices that "receive".

## Transmit devices

Devices that transmit will be automatically created by Domoticz, so we'll take a look at some of those first.

1. Go to 'Setup > Devices'.
2. n the "Search:" box type "rfx" or click the button "Not used" and press "Enter" to filter the devices to those created by the RFXtrx433E.
3. Click the green arrow (They are unmanaged) next to the device you wish to add.
4. Give the device a descriptive name in the "Add Device" popup and click "Add Device"
5. Your device will be added to the appropriate section in the Domoticz UI. 
6. For most devices Domoticz will gather and record appropriate data over a period of time.
7. By clicking on the "Log" button you can access graphs for your device

## Receive devices

Devices that receive need to be added to Domoticz manually.

1. Click on the "Switches" tab in the Domoticz UI, then click the "Manual Light/Switch" button upper left. [image](./images/Manual-add-Kaku-switch-screen.png)
2. From the "Hardware" dropdown list select "RFXtrx433E", then give the device a descriptive name.
3. Change the "Switch Type" field to "Dimmer" and the "Type" field to "LightwaveRF".
4. For the "ID" and "Unit Code" fields you need to select a unique combination - this is similar to how a LightwaveRF Remote Control would pair with a LightwaveRF device.
5. Place the LightwaveRF device into "pairing" mode by following the process detailed in the manual and click the "Test" button to complete the pairing.
6. Finally, click on "Add Device" to add the device to Domoticz. [image](./images/apnt-86_add_devices_from_rfxtrx433e_in_domoticz_10.png).
7. Domoticz will add a normal "On / Off" icon for the device, so we need to change that for a more appropriate "Dimmer" type. [image](./images/apnt-86_add_devices_from_rfxtrx433e_in_domoticz_11.png)
8. Click on the "Edit" button
9. Domoticz will show the device settings.
10. Change the "Switch Type" to "Dimmer" and click the "Save" button [image](./images/apnt-86_add_devices_from_rfxtrx433e_in_domoticz_13.png)
11. Domoticz will change the device icon to a fully functioning dimming control

Devices that can be learned by Domoticz.

1. Click on the "Switches" tab in the Domoticz UI, then click the "Learn Light/Switch" button upper right. [image](./images/Manual-add-Kaku-switch-screen.png)
2. As soon as Domoticz enters learning mode, click the device or remote control button that sets the device. [image](./images/kaku-learn-mode.png).
3. When the device is detected a window will appear where you can set its name, type and ID.
4. Write down the ID in the table below for future reference.

## My RFXCom devices and their ID's

The following devices are configured in Domoticz:
```
Hardware RFXtrx433XL
Switch type: on/off
Type: AC
Name                    ID              Unit code
Mechanische ventilatie: ID 0 01 01 01   UC 1
Vloerverwarming 1e:     ID 0 02 02 02   UC 2
TV simulator:           ID 0 04 04 04   UC 4
Schakelaar diversen 1:  ID 0 05 05 05   UC 5
Schakelaar diversen 2:  ID 0 06 06 06   UC 6
```
## Tip
When configuring and naming a device, put a pieve of tape on the device and write down it's name so you will know the correct devicename when you grab it.

## Adding the DANIU Mini portable 433MHz wireless thermometer

Adding this device to Domoticz was fairly simple. Follow steps below:

* Go to "Setup > Hardware > Click set mode @ RFXCOM" [image](images/Screenshotfrom2019-10-30-14-50-09.png)
* Enable the 'Rubicson' protocol and click "Set mode" [image](images/Screenshotfrom2019-10-30-14-50-55.png)
* Go to "Setup > Devices > Not used", You will see the Alecto WS1700 subtype appear with temperature and pressure. [image](images/Screenshotfrom2019-10-30-14-51-30.png)
* Click the green arrow in this line and add device with meaningfull name [image](images/Screenshotfrom2019-10-30-14-58-32.png)
* If necessary, edit blocky script to use Daniu thermometer in stead of zigbee
[images/](images/Screenshotfrom2019-10-30-15-01-33.png)6

Now use device.hh