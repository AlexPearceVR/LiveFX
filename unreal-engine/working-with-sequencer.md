# Working with Sequencer

Here are a few tips if you are using the sequencer.

## 1. Setting your camera in the Camera Cuts menu

To make sure your main camera is what is used when simulating the project:

1. Go to your sequence
2. On the Camera Cuts track, press the plus button
3. Select new binding
4. Select your camera

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

## 2. Loop your sequence

If you want to loop your sequence, follow these steps.

1.  Open the Level Blueprint\


    <figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>
2.  Drag off of **Event BeginPlay** and type **Create Level Sequence Player**\
    ![](<../.gitbook/assets/image (189).png>)


3.  Select your Level Sequence.\


    <figure><img src="../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>


4.  Right Click on **Settings** and select **Split Struct Pin**\


    <figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>


5.  Right Click on **Settings Loop** and **Split Struct Pin**\


    <figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>


6.  Select **Settings Auto Play,** and loop as many times as you want to, in this example, I'm looping 999 times. \


    <figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>
