# iPhone Apps

You can use an iPhone for basic camera tracking, but should only be used for R\&D purposes. All of the apps we have used so far are not good enough for Professional work.&#x20;

## Zig Sim Pro

Zig Sim Pro is an iPhone app that we can use for Camera Tracking in Live FX. It allows for x, y, z, pan, tilt and roll tracking.

{% embed url="https://youtu.be/LQPW4ii_S9A" %}

1. [Buy and Download Zig Sim Pro from the app store.](https://apps.apple.com/us/app/zig-sim-pro/id1481556614)
2.  In the app, Enable the ARKit by tapping just to the left of the name, you should see a checkbox. Make sure nothing else is checked.\


    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

    \
    The default ARKit settings should be fine, but if you click on the arrow, you can make sure they are set like this. Tracking Type Device and Feature Points On.

    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>
3.  Use the Settings mene and the Live Links menu and make sure you set your Port number the same, your device UUID the same, your IP address should match what is in Live FX, and change the Message Rate to 60.\


    <figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


4. Press Apply in the Live Links menu.&#x20;
5. Follow the [Camera Calibration and Nodal Offset instructions](../camera-and-lens-calibration.md)

## GyrOSC

You can find this app on the app store, and more information about it here. It's currently $.99

{% embed url="https://www.bitshapesoftware.com/instruments/gyrosc/" %}

Here is the Video Tutorial:

{% embed url="https://youtube.com/live/lzEZnJ3IH60" %}

1. Buy and [Download the app from the app store](https://apps.apple.com/us/app/gyrosc/id418751595)
2. Connect your phone and your computer to the same wifi signal
3.  In Live FX, go to the Live FX Menu, Live Links, turn on OSC App Sensor Tracker\
    \


    <figure><img src="../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>
4.  In the GyrOSC app, enter the IP address that you see in Live FX (purple). \
    Enter the Port number you wish to use in both programs (Green)\
    Create a "tag" and make sure it's spelled the same in both (Red)

    <figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>
5. On the Second tab, turn off all except Gyroscope, Accelerometer, Run in the Background, and try Frequency set to 60. \
   ![](<../../.gitbook/assets/image (194).png>)\

6. Make sure to press Apply to see the results.&#x20;

{% hint style="warning" %}
You will still need to do the [camera calibration and Nodal offset](../camera-and-lens-calibration.md) to get the best results.
{% endhint %}
