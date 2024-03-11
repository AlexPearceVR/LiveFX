# Control UE through OSC

## Overview

You can use OSC to do many things. We are going to create a layer in Live FX and use it to drive our Sun in Unreal Engine.&#x20;



Live FX currently has one way of using OSC that uses the first layer's Canvas transform controls, to control custom properties in Unreal Engine via a blueprint the user can set up.

There are a total of 9 float values that can be used in Unreal Engine, they correspond to the following properties in the Canvas menu (of the top dummy layer).&#x20;

The numbers here correspond to the Index numbers in the **Get OSC Message Float At Index** node in Unreal Engine

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

## Set up Live FX

1. Go to Live FX Menu>Live Links
2. Turn on OSC Sender
3. Turn On, enable Animation and press connect.&#x20;
4.  For your ip, if it's the local machine, you can use 127.0.0.1. For port, you can use 9003 or whatever port, but you'll need to remember this for later. \


    <figure><img src="../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>


5.  Create a new layer, and make sure it is the very top layer. This will be a "dummy" layer, do not add color grading or anything else to it. \


    <figure><img src="../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure>



## Set up Unreal Engine

You can find the whole blueprint here, copy and paste it into your Level Blueprint, and then connect the Event Begin Play to the Create OSC Server Exec pin. It may have some errors, but you should be able to fix them by following the instructions below.&#x20;

{% embed url="https://blueprintue.com/blueprint/m6-a4t3l/" %}
\\
{% endembed %}

Manual Instructions for creating the Blueprint.

1.  In your Level Blueprint (or you could create a new one), from **Event Begin Play**, add the node **Create OSCServer.** \
    \
    1\. For the IP Address you can use 0.0.0.0. \
    2\. For the Port use 9003 or whatever you set in Live FX\
    3\. Check Start Listening\
    4\. Write the same Server Name you added in Live FX for the Server Name. \


    <figure><img src="../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>


2.  Drag off of the Return Value pin and Promote to Variable and (optionally) rename the variable to OSCServer.\


    <figure><img src="../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>


3.  Then add **Unbind All Events from On Osc Bundle Received** and then add **Bind Event to On Osc Message Received**.\


    <figure><img src="../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>


4.  Drag off the Event socket, type **Create Event.** \
    Then in the dropdown select **Create a matching event.**\
    \


    <figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>
5.  **Rename** the event to **OSCMessageReceived** and press **Compile Blueprint.**\


    <figure><img src="../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>


6.  Drag off the Message pin and promote to a variable. The default name will be Message, we'll keep it the same for now. \


    <figure><img src="../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure>


7.  Drag off that node and Get OSC Message Float at Index, do this three times. \
    For the Index, we'll use 5,6 and 7.&#x20;

    <figure><img src="../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

    :bulb:Remember, the numbers that correspond in Live FX are the following from the top dummy layer:

    <figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
8.  From the left-side, drag over the Message Variable and select Get Message. \


    <figure><img src="../.gitbook/assets/image (265).png" alt=""><figcaption></figcaption></figure>


9.  From that variable, connect it to the three Get OSC Message Float At Index. \


    <figure><img src="../.gitbook/assets/image (266).png" alt=""><figcaption><p><br></p></figcaption></figure>


10. Draf off the execution pin of the last node, **Uncheck Context Sensitive** and search for **Set Relative Rotation**. Choose the **Transformation>Set Relative Rotation.**\


    <figure><img src="../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>


11. Right-click on New Rotation and select **Split Struct Pin**.\


    <figure><img src="../.gitbook/assets/image (268).png" alt=""><figcaption></figcaption></figure>


12. Drag the Value from **5 to the Z**, **6 to the Y**, and **7 to the X**. \


    <figure><img src="../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>


13. Drag your Directional Light from your scene into the blueprint. Then from the Blue output pin, connect that to the Target of the Set Relative Rotation. This will automatically create a node in between. \


    <figure><img src="../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>



## Control in Live FX

Back in Live FX, to control the X, Y, and Z, you click on the top layer, select the Canvas menu at the bottom left, and then you can use the Rotate X, Y, and Z to control the Sun in Unreal Engine (must be in play mode). \


<figure><img src="../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

## Custom Blueprints

You can create a blueprint and add many components to it, then you can go to the construction script and do some custom things to have one variable effect multiple components in different ways, in this example, multiplying the intensity variable so that it would be 10x the number that goes to&#x20;

<figure><img src="../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

Here is another example. For headlights in a city scene, we used a blueprint called "00\_BP\_Headlights",  which is a simple actor blueprint with a single Spot Light component.

Inside of each vehicle blueprint, we brought in this blueprint twice, these two act like the headlights.&#x20;

In the Level blueprint, we Get OSC Message Float At Index, then Get All Actors Of Class. We select the class 00\_BP\_Headlights, then add a For Each Loop, and set the intensity to the Value set in the OSC message.

<figure><img src="../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

