# Known Issues

There are several known issues that hopefully we can address in the near future, but you should be aware of them before starting down the Live FX > Unreal Engine road.&#x20;

1. Multi-Node setups are not easily setup or at least not well defined. It may be possible to set up a Multi-User Session and have one machine render the outer frustum and one machine ender the inner frustum, but this workflow has not fully been tested. So for now, we can only do inner frustum with real-time rendering.&#x20;
2.  You should test the Live Link auto-record and auto scene-take before using it in production, it currently gets off by at least one take after your first recording.\
    \
    For example, if you set the Slate to 1a Take 1 in Live FX, it will update the UE Scene to 1a Take 1. But when you press record and then stop the recording in Live FX, Live FX ups the take once, then in UE ups the take again, so in Live FX you'd be on 1a Take 2 and in UE you'd be on 1a Take 3.\
    \
    One thing you can do is to use the Auto Record function but do not use the auto-update scene-take function and just be VERY diligent in setting the correct Scene and Take in both Live FX and Unreal Engine. \


    <figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>
3. In Live FX, if the timecode source is sdi and there is no timecode coming through that sdi signal, it may lock the Unreal Engine Live Link.&#x20;
4.  You cannot record the Full Shot option from the Record settings and maintain a decent frame rate. If you want to record the composite you would need to find another way of doing so. \
    \
    One recommendation is to use an external recorder as your dual head, and record the composite onto that.\


    <figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Cannot Record the Full Shot</p></figcaption></figure>
5. Currently, there is no pipeline to import the USD that is recorded from Live FX and get that into Unreal Engine.&#x20;
6. The only way to control custom things in your scene directly in Live FX is a [short-term hack](control-ue-through-osc.md). You are better off building your own OSC interface using something like Open Stage Control if you need to fully control UE outside of UE.&#x20;

