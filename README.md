# Simple volume meter

I whipped this app up to show a basic volume meter on live audio input.  It does both clip detection and RMS volume.

A "volume" meter can mean many things; if you want to do clip detection, you really need to access every sample.  If you don't need clip detection, I might suggest using an Analyser and getByteTimeDomainData, since it will likely have lower CPU overhead.

It's also hosted at http://webaudiodemos.appspot.com/volume-meter/.

Check it out, feel free to fork, submit pull requests, etc.  MIT-Licensed - party on.

-Chris