# Projection Mapping 2.5d Workflow

You can manually set up a 2.5d shot with projection mapping by adding in layers and putting them in various Z-depth spaces, or project them on planes a varying depths. &#x20;

1. [Set your shot resolution](../getting-started/the-basics/change-shot-framerate-and-resolution.md) to the same resolution as your LED wall, or your preferred output resolution if Green Screen.&#x20;
2.  Add a Filler to the timeline and enter the shot.\


    <figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
3.  If you want to increase the shot duration, go to the Live FX Menu and change the out number to something longer, like 1000 frames. \


    <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>


4.  Right-click and import your files one at a time, you may want to click on "Still Frame" if you are importing images.\


    <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>


5.  After you add all your images, you can Shift+select them and Press Group. The order should go further back layer on top and closest layer on the bottom. Then with the Group selected, you may need to go to the Canvas menu and scale to fit.\


    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>


6. Go to the camera menu and [activate the camera](../getting-started/the-basics/general-tips.md#activate-the-camera).\

7. [Add a Version](../getting-started/the-basics/general-tips.md#add-a-version) and [Rename the version](../getting-started/the-basics/general-tips.md#rename-a-version) to "Parallax Node".&#x20;
8. Connect your tracker and make sure to Apply the tracking information.
9.  Go to the Camera menu, Config Tab and change the Far Clipping to something very far, like 10000\


    <figure><img src="../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>
10. For each layer, we need to go into the Canvas Menu, and move it back in Z depth, with the furthest layers further back than the closest layers. It might be helpful to reference the a[rticle on Cuebric about this](../cuebric-workflow/non-projection-mapping-with-cuebric.md#working-with-the-layers), which goes into more detail.&#x20;
11. For the Sky Layer, I'll set the **Trans Z to -5000**, enable the **Fit** **button**, and then turn off **Relative button.**\


    <figure><img src="../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

    I'll repeat this for all the layers with the Trans Z being the following for each layer:\
    Water -3000\
    Mountains -250\
    Dome -42\
    Rocks -11
12. With the main Group layer selected, go to the Plug-ins menu, find the Plane->Wall plugin and **Apply On Node**
13. Open the the Plane->Wall menu, click on Link to Stage Manager, and select the appropriate wall. (You may need to go to the stage manager and make sure the wall is active).\


    <figure><img src="../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>


14. Click on the Projection Tab and Link to Shot Camera.

(More details needed, check back again soon).
