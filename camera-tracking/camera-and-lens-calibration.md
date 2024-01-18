# Camera and Lens Calibration

Currently, Live FX can only work with Prime Lenses or at fixed focal length for calibration.&#x20;

For example, if using an 18-55mm Zoom lens. You could calibrate it at 18mm, 24mm, 35mm, and 50mm

When you make your calibration, make sure your shot resolution and frame rate are correct.&#x20;

{% hint style="info" %}
You may want to create a new timeline and shot specifically to make your calibration.&#x20;
{% endhint %}



**Leave the Sensor at Generic** and default Width, Height, and Crop factor of 1.&#x20;

Change your focal length to the lens size that you are using on your camera.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

\*Maybe you don't type in your sensor size? if you do, you have to work with crop factor and make sure the aspect ratio is correct, that what you see in your camera viewfinder is the same that is in live fx, there is no cropping or scaling happening.

{% hint style="info" %}
It's important that after you do your calibration, the focal length in Live FX Camera is very close to or the same as the physical lens on your camera.&#x20;

For example, if your lens is 24mm on your camera, the calculated Focal length in Live FX should be close to 24mm.&#x20;
{% endhint %}



{% hint style="danger" %}
If entering in sensor size, **make sure to get the correct sensor size and crop** factor from your camera manufacturer, and make sure you calculate it based on the **Resolution Setting** and **Aspect Ratio** you are using.&#x20;

For example, Red Cameras:

At 6k 16:9 the crop factor is 1.49x and the Focal Lenth is 35.7.\
At 6k 17:9 the crop factor is 1.42 and the Focal Length is 34mm.
{% endhint %}

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption><p>At 6k 16:9, the crop factor is 1.49x and Focal Length is 35.7mm</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>At 6k 17:9, the crop factor is 1.42x and Focal Length is 34mm</p></figcaption></figure>

