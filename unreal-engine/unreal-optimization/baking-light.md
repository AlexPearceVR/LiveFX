# Baking Light

Light baking is an excellent way to improve performance, but it is somewhat of a balancing act to make everything work correctly. Here are a few tips up front:

* Use GPU Lightmass Plugin
* If you have moveable objects in your scene, set them to movable and lighting to stationary (not static)

## GPU Lightmass

### Project settings

1.  Go to Edit>Plugins. Search for GPU Lightmass and Enable\


    <figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


2.  Go to Edit>Project Settings. Search Hardware Raytracing and Enable **Use Hardware Ray Tracing when available** and **Support Hardware Ray Tracing**.\


    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


3.  Also in Project Settings, search Virtual Texture and check **Enable Virtual Texture Support.** \
    \
    **MAKE SURE TO ENABLE VIRTUAL TEXTURE LIGHTMAPS AS WELL.** \


    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


4.  Also in Project Settings, search Global Illumination and change to None.\


    <figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
5.  Probably not needed, but you can also go to your post-process volume and change your Global Illumination to None and Reflections to None.\


    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


6. Restart your project.

### Set up your lights

You will want to go through all of your lights and environment lighting and determine if you want them to be static or stationary. If unsure, just use Stationary.\


<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You may want to set your Skylight to Real Time Capture.\


<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

I will change these point lights to Stationary as well.&#x20;

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Set up your Objects

You need to determine which objects in your scene need to be set to Static, Stationary, or Moveable. \


<table><thead><tr><th width="197"></th><th width="353"></th><th>Examples</th></tr></thead><tbody><tr><td>Static Objects</td><td>Will not move at runtime at all. </td><td>Buildings</td></tr><tr><td>Stationary Objects</td><td>Objects might need to move but are not always moving.</td><td>Props that may be moved at runtime</td></tr><tr><td>Movable Objects</td><td>Objects need to move constantly.</td><td>Animated Cars</td></tr></tbody></table>



### Baking

Go to Build>GPU Lightmass to open the window.\


<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the GPU Lightmass tab, uncheck "Viewport Realtime is OFF".&#x20;

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you cannot turn of Viewport Realtime is off from this menu, go to the Viewport Options at the top left of the viewport and there will be something that says "Disable Realtime Override".\
![](<../../.gitbook/assets/image (11) (1).png>)\

{% endhint %}

Click on Build Lighting at the top left of the GPU Lightmass window.\


<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### Tips and Troubleshooting

You can change your Lighting Quality by going to Build>Lighting Quality

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

You should check your Lightmap Density and Resolution Adjustment by going to Build>Lighting Info

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

With static lighting, especially where you have very large objects, like the ground, you may need to click on the object, search for "Lightmaps", and override the Light Map Res to be much much larger.&#x20;

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

## References

Here are a few video references that have been helpful for us:

Baked RTX Lighting in Unreal Engine 5\
[https://youtu.be/2VY-ZBWM5-M?si=HYBETr4aIFUh5lUV](https://youtu.be/2VY-ZBWM5-M?si=HYBETr4aIFUh5lUV)

UE5 Can we still Bake Light?\
[https://www.youtube.com/watch?v=Tx-PNbKmLPU](https://www.youtube.com/watch?v=Tx-PNbKmLPU)
