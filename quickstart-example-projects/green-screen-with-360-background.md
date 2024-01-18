# Green Screen with 360 Background

To follow along with this Example, y[ou can download this 360 video file ](https://www.dropbox.com/s/tyrjytmfwq0ufik/HMB\_BoatShort.mp4?dl=0)and use it for your background.&#x20;

[Set up your project](../getting-started/the-basics/project-settings.md) with the right frame rate and resolution.&#x20;

Once you enter the project.

Choose "Live Setup" and then choose Green Screen with Background from the dropdown menu which will open the Create Live Composition window.

<figure><img src="../.gitbook/assets/image (32).png" alt="" width="563"><figcaption></figcaption></figure>

Foreground Camera - Choose the Live Capture source from the capture card that you have already set up in your [Video IO settings](../getting-started/introduction/settings/video-io-settings.md). I'm using my Mac's built-in webcam for this example, but normally I'd be using the camera signal coming into my Blackmagic Decklink 8k.&#x20;

Background - Click on Browse and choose a 360 Video.&#x20;

{% hint style="info" %}
Make sure that Equirectangular is "On" if using a 360 video or image.
{% endhint %}

If you have already set up a Camera Profile and Camera Tracker, go ahead and choose those now as it will save you some time. Otherwise, continue on and you can create a camera profile and set up camera tracking later.&#x20;





