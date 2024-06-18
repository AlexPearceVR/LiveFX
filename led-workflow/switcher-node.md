# Switcher Node

If you need all walls to go out the DualHead via Nvidia Mosaic, then you need Stage Manager, even though you‘re not using any projection.

If you want to send one wall via dual head, one via SDI, or 4 walls via individual SDI channels, then no need for Stage Manager.

1. **Select your clips**, in this example 3 clips.
2.  Hit the **Switcher** button under the Utilities\


    <figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


3.  This will create a new shot that will stick to your mouse, bring it over to the Left side menu, and with your mouse over Add, left click, which will create a new Timeline with this switcher node.

    <figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
4. Drop the Shot on the timeline and then double-click on it to enter the shot.\

5.  With Primaries selected, go to the Switcher menu and click on Channel Controller, then go to the Displays tab.\


    <figure><img src="../.gitbook/assets/image (9) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


6. Route all your inputs to your SDI outputs, or to Dual Head as needed.

{% hint style="info" %}
I don't have a capture card with SDI outputs, so I cannot show what that looks like in a screenshot.&#x20;
{% endhint %}

With stage manager it‘s similar, but you need to define the walls in there and position them in the mapper tab.&#x20;

After that, it‘s a similar workflow, where you wrap all shots into a switcher node and point the dual-head output to output the stage mosaic.&#x20;

{% hint style="info" %}
The stage mosaic may require a unique switcher node that is only created through the Projection Setup Panel instead of a normal switcher node or it may need a project node (e.g. Frustum to Wall, etc.)
{% endhint %}
