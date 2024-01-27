# How to Package an Unreal Engine Project for Live FX

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

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>
