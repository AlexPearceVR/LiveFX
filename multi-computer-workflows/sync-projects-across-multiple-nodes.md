# Sync Projects across Multiple Nodes

Until we have a more streamlined workflow for Multi-Node workflows, you can use tools like Free File Sync to push new changes from your master machine to your client machines.&#x20;

Some IT knowledge will go a long way in setting this up.&#x20;



## Setup

Before we get setup let's go over a few things.

If you have a shared media server, you should be able to use to add new media to your project. If not, you'll need to sync the media location local path that is the same for all machines.



This way, you can add media to each machine in the same folder and Live FX will know where to look for it. Also this way&#x20;

### Create the initial project

First let's create the initial project that we are going to sync. Let's first create it on the Master machine. I will create a project called "00\_SharedProject" and use the default settings for now.&#x20;

Now let's go to the client machine and create a project with the exact same name.&#x20;



### Shared folder for the Media

1. Make sure your computers are on the same network and can ping each other.&#x20;
2.  On the client machine, let's create a shared folder for wherever you are going to store your media. \
    \
    For now, I will do this in the same location as my project, but this can be anywhere you want to store the media. I will name this folder "Media". \
    \*it should be a fast nvme or ssd drive if you plan to playback high-resolution media.\


    <figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
3.  &#x20; From the Live FX start menu, go to your project settings,&#x20;

    <figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

    Now change your Media Path to be the new folder you created. \


    <figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>
4.  In File Explorer, navigate to the Media folder, right-click the folder, go to Properties, then go to the Sharing Tab and click on "Share".\
    \
    \*You must be the admin of both machines and you may need both machines to have the same Username and login credentials.\


    <figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>


5.  If you don't already have an "Everyone" under the name, click on the dropdown and select "Everyone".\


    <figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>


6. With Everyone selected, click on share.
7.  Find the path to this folder by right-clicking on the folder and going to properties, then the share tab again. Here it will say Network Path: and give you the path. Notice that "Media" is left out, you will have to add "\Media" to the end of this path. \


    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>


8. Now let's find the IP Address of the client computer. You can do that by pressing the windows key and searching for "Command Prompt". \
   \
   In the command prompt, type in ipconfig, then find the relavant IPv4 address. In this case, mine is 192.168.1.41. Save this for later. \
   \
   ![](<../.gitbook/assets/image (14).png>)\

9.  Now on the Master Computer, from File Explorer, right-click on the "This PC" icon and press "Map Network Drive"\
    \


    <figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>


10. Select an unused Drive Letter, like V.\


    <figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>


11. Under the folder, type in \\\ + the ip address of the client compuer + the path (minus the computer name). \
    \
    In this case, I would type \\\192.168.1.41\Users\Demon\Videos\00\_SharedProject\Media
12. Keep reconnect at sign-in and press Finish.&#x20;
13. Now you can access this folder from your master machine, and anything you add to it will automatically be put into the folder.&#x20;





