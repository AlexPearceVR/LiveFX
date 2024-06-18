# Working with Mattes

You can use black and white mattes in various ways in Assimilate.&#x20;

Let's say we want to bring in a Z-Depth Matte, to control the Depth Of Field of our scene.

1. Make sure your [Z-Depth Layer channels are mapped correctly.](re-map-exr-channels.md)
2. Create a new layer from the left panel.
3. Fetch or Import your matte.
4. Go to the Fill/Matte Menu.
5.  Drop the matte in the "Drop Layer Matte" field\


    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
6.  Change the layers to NOT use the Alpha channel. \
    This is incorrect:

    <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>The matte is not correct because the Alpha channel is enabled and black and white mattes do not contain an alpah channel.</p></figcaption></figure>

    This is correct:

    <figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>With the A turned off, the matte looks correct.</p></figcaption></figure>



Now that the matte is set up, any adjustments that we make to this layer will use the Matte to influence the effect.&#x20;
