# Using External Antennas with ODK or GeoODK

* [Overview](#overview)
* [Catalyst Setup](#catalyst-setup)

## External Antenna Overview {#overview}

_work in progress_

### Trimble Catalyst Set-Up {#catalyst-setup}

![](/assets/catalyst/catalyst.png)

Let’s walk through how to set it up… 

What you will need to get started:
1. An Android smartphone or tablet that has a data plan (this is a potential weakness of the Trimble device - GPS corrections require an available network, which isn’t always possible in remote areas);
2. A Trimble Catalyst antenna;

![](/assets/catalyst/2m-accuracy.png)

3. The Trimble Catalyst and Trimble Mobile Manager application (which can be downloaded from the Google Play Store);
4. Your own Trimble account; 
5. Enabled “Developer Tools” on the Android device to change the phone from using the native GPS receiver to using the Catalyst device. (You can enable developer tools on your Android by going to Settings > About phone > Build. Click “Build” seven times and the developer mode will be enabled.); and
6. (Optional) A rod/tripod to mount the antenna for stability/accuracy.  
7. (Optional) An extra battery or power bank for your phone as the Catalyst can quickly drain a phone battery.

How to Use the Catalyst with OpenDataKit:

Open the Trimble Mobile Manager application to log in to the Trimble Catalyst app. This app is used to manage the antennae and the Catalyst subscription.

Plug the Catalyst into USB charger/accessory port of your phone and wait for the Catalyst to pick up the satellites. The satellite icon will appear green (as shown below) when coverage is sufficient. 

![](/assets/catalyst/developer-options-3.png)

Now for the trickiest part, click the “Setup” section in the app to view the instructions that describes how you can reprogram your phone to read the Catalyst coordinates instead of the smart phone receiver. This is when you will need to have the Developer Options enabled. 

![](/assets/catalyst/developer-options-2.png)

To do so, you need to start by going to “Settings”, scroll down to “System”, click on “Developer Options” and scroll down until you find “Select mock location app”.  Once clicked, you should see “Trimble Mobile Manager” listed. 

![](/assets/catalyst/developer-options-3.png)

Choose that option so that ODK can use the Catalyst to collect two to three meter accuracy.

![](/assets/catalyst/2m-accuracy.png)


And finally, start mapping!

You will know if it is working by the Catalyst icon on the top of your screen and when you collect a point with ODK Collect and see that you have two meter accuracy!  Woot woot!

##### Troubleshooting:
1. When first connecting with satellites, you need to be outside with a clear view of the sky. Once the satellites are engaged, you can work under canopies or in between buildings.
2. Subscribe before you set-up. You cannot change your subscription settings from the app so we recommend that you subscribe before you going into the field. 
3. Make sure your phone is sufficiently connected to data. The centimeter level accuracy only works when you have cellular data. 
4. Make sure you are using the correct type of phone. The Catalyst, like ODK Collect and GeoODK, is only supported on Androids.



