# Camera and Lens Calibration

{% embed url="https://player.vimeo.com/video/727369885" %}

{% hint style="danger" %}
When you are in the Setup menu for Camera Calibration, make sure you measure the Square separately from the Aruco. The square values are on the Left (orange) and the Aruco Size is on the Right (purple).
{% endhint %}

<figure><img src="../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

Currently, Live FX can only work with Prime Lenses or at fixed focal length for calibration.&#x20;

For example, if using an 18-55mm Zoom lens. You could calibrate it at 18mm, 24mm, 35mm, and 50mm, but it cannot dynamically change as you zoom.

When you make your calibration, make sure your shot resolution and frame rate are correct.&#x20;

{% hint style="info" %}
You may want to create a new timeline and shot specifically to make your calibration.&#x20;
{% endhint %}

**Leave the Sensor at Generic** and default Width, Height, and Crop factor of 1.&#x20;

Change your focal length to the lens size that you are using on your camera.

<figure><img src="../.gitbook/assets/image (24) (1).png" alt=""><figcaption></figcaption></figure>



If you do enter your sensor size, you have to make sure the aspect ratio and crop factor are correct.

What you see in your camera viewfinder should be the same in Live FX with no cropping or scaling.

{% hint style="info" %}
It's important that after you do your calibration, the focal length in the Live FX Camera is very close to or the same as the physical lens on your camera.&#x20;

For example, if your lens is 24mm on your camera, the calculated Focal length in Live FX should be close to 24mm so that it will forward 24mm to Unreal Engine.&#x20;
{% endhint %}

{% hint style="danger" %}
If entering in sensor size, **make sure to get the correct sensor size and crop** factor from your camera manufacturer, and make sure you calculate it based on the **Resolution Setting** and **Aspect Ratio** you are using.&#x20;

For example, Red Cameras:

At 6k 16:9 the crop factor is 1.49x and the Focal Length is 35.7.\
At 6k 17:9 the crop factor is 1.42 and the Focal Length is 34mm.
{% endhint %}

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption><p>At 6k 16:9, the crop factor is 1.49x and Focal Length is 35.7mm</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption><p>At 6k 17:9, the crop factor is 1.42x and Focal Length is 34mm</p></figcaption></figure>

