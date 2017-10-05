# Using External Antennas with ODK or GeoODK

* [Overview](#overview)
* [Catalyst Setup](#catalyst-setup)
* [Garmin GLO Setup](#garmin-setup)

## External Antenna Overview {#overview}

The external GPS antennae market is growing. At the moment, there are more than a dozen competitive devices for sale that allow users to enhance the accuracy of the native GPS receiver in a smart phone. Both Cadasta and our partners have worked with a range of external antennas in the field, with varying results. Here are a few guides to get you started with using an external antennae!

### Trimble Catalyst Set-Up {#catalyst-setup}

<img src="/assets/catalyst/catalyst.jpg" width="400" />

Let’s walk through how to set it up… 

What you will need to get started:
1. An Android smartphone or tablet that has a data plan (this is a potential weakness of the Trimble device - GPS corrections require an available network, which isn’t always possible in remote areas);
2. A Trimble Catalyst antenna;

![](/assets/catalyst/trimble-apps.png)

3. The Trimble Catalyst and Trimble Mobile Manager application (which can be downloaded from the Google Play Store);
4. Your own Trimble account; 
5. Enabled “Developer Tools” on the Android device to change the phone from using the native GPS receiver to using the Catalyst device. (You can enable developer tools on your Android by going to Settings > About phone > Build. Click “Build” seven times and the developer mode will be enabled.); and
6. (Optional) A rod/tripod to mount the antenna for stability/accuracy.  
7. (Optional) An extra battery or power bank for your phone as the Catalyst can quickly drain a phone battery.

### How to Use the Catalyst with OpenDataKit:

1. Open the Trimble Mobile Manager application to log in to the Trimble Catalyst app. This app is used to manage the antennae and the Catalyst subscription.

2. Plug the Catalyst into USB charger/accessory port of your phone and wait for the Catalyst to pick up the satellites. The satellite icon will appear green (as shown below) when coverage is sufficient. 

<img src="/assets/catalyst/developer-options-1.png" width="300" />


3. Now for the trickiest part, click the “Setup” section in the app to view the instructions that describes how you can reprogram your phone to read the Catalyst coordinates instead of the smart phone receiver. This is when you will need to have the Developer Options enabled. 

<img src="/assets/catalyst/developer-options-2.png" width="300" />

4. To do so, you need to start by going to “Settings”, scroll down to “System”, click on “Developer Options” and scroll down until you find “Select mock location app”.  Once clicked, you should see “Trimble Mobile Manager” listed. 

<img src="/assets/catalyst/developer-options-3.png" width="300" />

4. Choose that option so that ODK can use the Catalyst to collect two to three meter accuracy.

![](/assets/catalyst/2m-accuracy.png)


5. And finally, start mapping!

You will know if it is working by the Catalyst icon on the top of your screen and when you collect a point with ODK Collect and see that you have two meter accuracy!  Woot woot!

##### Troubleshooting:

![](/assets/catalyst/screens.png)

1. When first connecting with satellites, you need to be outside with a clear view of the sky. Once the satellites are engaged, you can work under canopies or in between buildings.
2. Subscribe before you set-up. You cannot change your subscription settings from the app so we recommend that you subscribe before you going into the field. 
3. Make sure your phone is sufficiently connected to data. The centimeter level accuracy only works when you have cellular data. 
4. Make sure you are using the correct type of phone. The Catalyst, like ODK Collect and GeoODK, is only supported on Androids.


### Garmin GLO Set-Up {#garmin-setup}

1. Charge the battery (about three hours). Fully charged battery lasts about 12h according to manual. 
2. Turn on the GPS
3. Enable Bluetooth in the Android device
4. Pair the GPS device with the Android device via Bluetooth
5. Download Bluetooth GPS app in Google Play
6. Open the Bluetooth GPS app
7. Select “Garmin GLO” as the select paired GPS device, and enable “Mock GPS Provider”

![](/assets/catalyst/garmin-1.png)

8. You may be redirected to Android settings to enable “Allow mock locations”. I think this is different device by device. In mine was this process: 
	A. Go to Settings > System > Device Information > Clicking 3 times in “Build Information”
	B. Developer Menu appears under Settings > System > Developer Menu
	C. There is an option to “Choose application to mock your location, and then you select "Bluetooth GPS". 
	D. I have seen in the Garmin user manual and in some videos in youtube that in some cases it’s just a checkbox for enabling “Allow mock locations”
9. Go back to the app and click on “Enable Mock GPS Provider” if needed

![](/assets/catalyst/garmin-2.png)

10. Click on the ellipsis menu on the top right corner 
11. Tab on Settings
12. Enable Reconnect Option 
13. Setup Reconnect Interval to just the minimum option (5 seconds)
14. Go back to the main menu of Bluetooth app and click on Connect
15. Open ODK 
16. Start collecting data and notice the greater accuracy on the coordinate collection!


