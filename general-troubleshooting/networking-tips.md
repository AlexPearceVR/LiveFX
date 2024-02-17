# 🖥 Networking Tips

## How to find your computer's IP Address

### Windows

1. &#x20;Press the Windows key, type **Command Prompt** and open
2.  Type in **ipconfig** and press enter\


    <figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>
3.  Find the ip address you are looking for. \
    Ethernet adapters will be listed as well as any Wireless adapters. You are looking for the **IPv4 address.**\


    <figure><img src="../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>



### Mac

1. Search for the Mac app Terminal
2.  type in ifconfig and press enter\


    <figure><img src="../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>


3.  Find for the ip address you are looking for. On my Mac, usually en0 is the wifi

    <figure><img src="../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>



## How to ping a device on the network

If you are trying to connect to a network, you can use the ping command to troubleshoot if the computer can talk to the device you are trying to connect to.&#x20;

1. (Windows) Click on Windows and search for Command Prompt. \
   (Mac) Search Applications for Terminal.
2.  Type in "ping" then the address you want to ping, with a space between ping and the address. For example I would enter "ping 192.168.1.1"\
    \
    If the ping is successful, it will show a number and **bytes** from the address like in this screenshot:\


    <figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

    If the ping is unsuccessful, it will say **Request timeout**.\


    <figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>


3. To stop the ping, close the terminal window or press Control+C (Mac and PC).&#x20;
