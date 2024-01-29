# Packaged Unreal Engine project Example

## Overview

The Live FX/Unreal Engine workflow allows you to **build your Unreal Engine Projects to a game,** that can exist as an .exe file.&#x20;

This means that if you plan ahead and [package your project](../unreal-engine/how-to-package-an-unreal-engine-project-for-live-fx.md), your Unreal Project can work **without Unreal Engine even installed** on the host machine, complete with camera tracking, projection mapping, and Web Remote Control if you need it!&#x20;

If you want to follow along with this example, you do not need to have Unreal Engine installed, just a Windows computer with Live FX already installed and set up.

Here is a complete video walkthrough:

{% embed url="https://youtu.be/gBtlxkdA36U" %}

## 1. Download Example Packaged Project

Here is a demo exe file:\
[https://www.dropbox.com/scl/fi/tfnwx5b8hkuy4cavxd4ku/WaterTower\_v2.zip?rlkey=fshkrjb1sw8h2c5a8sjvoj4if\&dl=0](https://www.dropbox.com/scl/fi/tfnwx5b8hkuy4cavxd4ku/WaterTower\_v2.zip?rlkey=fshkrjb1sw8h2c5a8sjvoj4if\&dl=0)

Download the .zip folder above.&#x20;

![](https://lh7-us.googleusercontent.com/GhJiYiWhsh3NkATbQJxjsJ7FOYUsx\_Z5yO55Bu9zAy6vXMl06xBIYd0PF2r8LNrn7GDk9p8koO21K0ttdGDa-bTchBJ4e0xyVDptlf3t5l438qaNJfGQ1TbezJB7wIUqVrxmQEcv\_2JqtPss004mto4)![](https://lh7-us.googleusercontent.com/kGL5Y0PYLE9o4NThdA28x058K-6n8-RDdvMsrSKKzuz0VAyOJzJlaMfIyLarDqhzKxHxjWCH6a0\_kRZo8MbDInq6S7gT99YW\_5NrKqO0rRAie00F9SzXBWpdjE0lmTPYSrecMpQqPprCoPbSObX5SR8)

{% hint style="warning" %}
EXTRACT WITH A TOOL LIKE 7 ZIP! The default Windows tool sometimes gives an error when trying to unzip large files.
{% endhint %}

In the folder structure, you will find the project “BH\_Project.exe”.&#x20;

If you open this, it will launch a full-screen game, but for it to work properly we’ll have to create a shortcut and **pass some command line arguments in.**

Even if there is a shortcut provided, you will likely need to make your own shortcut for this to work properly.

\


<figure><img src="https://lh7-us.googleusercontent.com/7M1tZWQjKKq66W3-0EWqADdloiVPQ6VoO4-VL-hAiwwSaS49-xYExfvVr-0pec6LfhIzTH3CdxL0mlXOk4_qwAx0c6R2erxFRE3mNagctBNC2J6oNYojxBMHGjfottlvUVL3i-mFIOB81kcQg-tvRY4" alt=""><figcaption></figcaption></figure>

## 2. Create a shortcut

1. Right-click on the BH\_Project.exe, and go to **Create shortcut.**

![](https://lh7-us.googleusercontent.com/7B4ZwGp5A50dc6l2kKjrRHI8DcbG0Rxi6ZjoG4nVnSNrVIiKRVIobHQ1pRueV\_7\_0d9wBvDBrTzpT6D2ikjUy4001anxzxJr-QlwiS1X7zE\_ObNG7stH-3jTttScZCL9EKkjICOCK9-AAEZ8hT8rJSk)

I’ve renamed the shortcut to “**OnScreen1920x1080**”

2. Now right-click and go to properties on the shortcut.

![](https://lh7-us.googleusercontent.com/Q7EVFiQIzghzeuWfx\_-2LFPd\_wL5nPFTrjUKW8OVFCYwaTtp8UZpGKqXk0CA2jqTJPqyxPNjw0gIKoc6Q\_TDM-AiNXXNLmO7xgR45on48x53irZughNvgh8qb8oKD-d7WogGLVgY1dPHniFKbYcc0Bk)

3. Paste these in the **target** field, after “...exe”, with one space after the end (with or without -RenderOffscreen, if you want to be able to see it or not).\
   \
   Text to copy and paste:\
   **-RenderOffscreen -ForceRes -ResX=1920 -ResY=1080 -RCWebControlEnable -RCWebInterfaceEnable**\
   \
   Should look like this:\
   ![](https://lh7-us.googleusercontent.com/wHpA5cBq7rQlfq8DxcrDcz8zVKW-R6VQQKYiTSN2JhrdwtLXvQjd87HwovQl8wSFlnNn--dcUcK0pC2SMBDVNMfugLMRWW87aP7y4hWG8aOiK37v2mJ9j9XR2ilML2JN59fQc3ndxXdNCousI9RYClw)
4. You should enter the resolution of your LED wall, or your monitor, as you want. So if your wall is 2560x1320, you’d put **“-ForceRes -ResX=2560 -ResY=1320”** where it’s appropriate.\
   \
   And you would likely want to [change your timeline resolution](../getting-started/the-basics/change-shot-framerate-and-resolution.md) to match this setting as well.&#x20;

{% hint style="danger" %}
IF YOU ARE RENDERING OFFSCREEN, YOU WILL NOT SEE THE EXPERIENCE LAUNCH, PRESS **CONTROL+ALT+DELETE** TO SEE IT AND TO CLOSE IT.
{% endhint %}

## 3. Open the Example Project

Now open the **shortcut**, if rendering offscreen you will not see it, **but Live FX will**.&#x20;

## 4a. Green Screen Setup

There are a few different ways we can set up a shot with Unreal in the background.&#x20;

If using an LED Wall, skip to the next section, [Projection Setup](packaged-unreal-engine-project-example.md#id-4b.-projection-setup)

If you are using a Green Screen workflow, go to the construct press the Live Setup button, and **choose Green screen with Unreal background for the Model.**

Under Unreal Capture, select **Unreal Texture Share.**

<figure><img src="../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

## 4b. Projection Setup

From the construct select **Projection Setup**, under Project Media, select **Unreal Texture Share.**&#x20;

Then follow whatever projection mapping methods you normally use.

<figure><img src="../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

## 4c. Basic Capture

If you want to play the UE project on the wall, but skip the Projection mapping workflow, you can just click Live Setup, then Basic Capture, and under Foreground / Camera, choose Unreal Texture Share.

For this tutorial, I will use this last option, Basic Capture, but the next steps are the same, regardless of your setup.

<figure><img src="../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

## 5. Set up Unreal Live Link

1.  Click on the **Live FX** menu, then click on the **Live Links** Menu.\


    <figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>
2.  Click on **Unreal Live Link.**\
    **Press On.**

    (Optional) Click Broadcast.

    **Click Connect.**\
    \
    If you see numbers moving at the bottom, this is set up correctly.\


    <figure><img src="../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

    IP can be 127.0.0.1 if using the local machine\
    \
    The Port should remain 9001.
3.  If using **camera tracking**, make sure your tracking is set up correctly and that you **press “Apply”** so that it applies to your camera.\
    \


    <figure><img src="../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>


4.  If **not** using camera tracking, go to the **Camera tab and press “Active”**

    You can manually move the camera in UE, by changing the Tracker / Animation values.\


    <figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

We can see from the screenshot below that we’ve set everything up correctly because we see the Watertower demo in the viewport (through the Unreal Texture Share layer), the Live Link has a frame counter, **counting frames** below the Scale in the Unreal Live Link window. \


In the **Camera tab**, the camera is active and if I pan, it moves the Unreal Engine camera. If you have camera tracking enabled, when you move the camera, it should move correctly.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/8IHYVi_4BqtN2FYJGZ90KKZPGlMv7hNlR_T4ygXFsM8ZGoQtbFX-CvxQi36sDsFVuAraTU5q_KqD59FUgbgz05z-TrB8dSdfQoLsUS__Xl_cW4moXxZXwPlE77eUIVzsZrGQ1pHmFQF7auq5yFPqNng" alt=""><figcaption></figcaption></figure>

## 6. Web Remote Control&#x20;

With the WaterTower demo working, and if you passed the\
&#x20;**-RCWebControlEnable -RCWebInterfaceEnable** flags in the shortcut link before you launched it, you should now be able to **control** certain aspects of the Unreal Engine scene.

Open a browser and enter **“localhost:30000”**

<figure><img src="https://lh7-us.googleusercontent.com/ViLHLr0w3x4X6ikVOLebrGICrSwSYpsli8y5_utEhBsXY0zN7O6ELOeEmcd1xsCd-CxCZR4gu-KZ1t8xvdqddt0QOZNH0Ugi7WzvMBflPucoOcHKpuboXUfIeedkvDgZe8xWJwi6ziCiTYmwxv0-1g0" alt=""><figcaption></figcaption></figure>

You should see this window above and be able to control the time of day, and cloud coverage as well as many other parts of the Unreal Engine scene, in this example **I changed the time to 1800 (6pm).**&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/6Oi0qliYhsQx0dSEI_4AwS-sfibaSiMi_72wBduGDI-q5A09KtQyYjMoP171acmW5o1L_6KoSnE5kZKqeFyVdRy1YZ4TTctBXcAkY7AwiY4i6tJ_EN-wDLSgWgVtNm7uhfmYW_mDpN5fNtYKoXItF1Q" alt=""><figcaption></figcaption></figure>

