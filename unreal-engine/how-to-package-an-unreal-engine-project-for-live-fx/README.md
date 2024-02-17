# How to Package an Unreal Engine Project for Live FX

## Package Project

Packaging a project is the same thing as building a game.&#x20;

{% hint style="warning" %}
The first time you package your project, it has to cook everything and it usually takes a long time, but after the first successful build, it usually takes a fraction of the time. For example, it might take 30 minutes to build the first time, and 2 minutes to build the second time.
{% endhint %}

{% hint style="info" %}
Some errors you get may be due to plugins that are enabled and do not need to be packaged. For example, I had Nvidia's OptiX denoiser and I got an error that stated&#x20;
{% endhint %}

To package your project, go to **`Platforms>Windows>Package Project.`**

Navigate to a folder where you want it to go and press accept.

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

## Change game mode Default Pawn to none

If you don't do this, then when the camera is not moving for 5 minutes or so, it will jump out of the camera and won't allow you to move the camera anymore.&#x20;

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You should also be able to change the game mode by using a console command.
{% endhint %}

## Enable Remote Session

If you haven't done so already, make sure to enable the Plugin "Remote Session", which allows iPhones and iPads to connect via the web remote control.&#x20;

## Copy Webapp into Packaged Project

For web remote to work correctly, you need to copy over a specific folder and create a specific folder structure in the built folder.&#x20;

1. **Copy** the folder **Webapp** from your Unreal Engine folder, normally located in:\
   C:\Program Files\Epic Games\UE\_5.3\Engine\Plugins\VirtualProduction\RemoteControlWebInterface\WebApp
2. Navigate to the built folder, go into Windows\Engine\Plugins\
   By default, there is only a folder called Runtime in there.&#x20;
3. Create a new folder here called "**VirtualProduction"**\
   **\*Make sure to spell it exactly like VirtualProduction with caps and no space in between.**
4. Inside VirtualProduction, create another folder called "**RemoteControlWebInterface**"\
   **\*Make sure to spell it exactly like RemoteControlWebInterface with caps and no spaces in between.**
5. **Paste** the **WebApp** folder here.&#x20;
6. Check and make sure your paths and folders look correct, if done correctly it should look like this:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Change Project Name

To change the project name (what shows up when you open the Task Manager), you can go to the DefaultGame.ini file and rename the "ProjectName" to what you want.

<figure><img src="../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

## Working with Sequencer

To start an animation sequence at the start, and to have it loop 999 times, set up your Level Blueprint like this:\


<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
To break out the settings, right-click on the Settings pin and select "Split Struct Pin".![](<../../.gitbook/assets/image (12).png>)\

{% endhint %}



## Change Levels

In order to be able to change levels with Command Line Arguments, you will need to make sure you package your game with the levels you need to be able to load.

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

Then to open your map, you need to know the path that you put here, and paste it exactly as it is after the ...exe, with no "-". For example, it should look like this:\


<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

If you want to add any command line arguments, they would go after the map path. For example, this is how the whole path might look, notice the spaces. \
\
"C:\Users\Windows\LightSail.exe" /Game/StarterContent/Maps/Minimal\_Default -RenderOffscreen
