# Simple volume meter

I whipped this app up to show a basic volume meter on live audio input.  It does both clip detection and RMS volume.

A "volume" meter can mean many things; if you want to do clip detection, you really need to access every sample.  If you don't need clip detection, I might suggest using an Analyser and getByteTimeDomainData, since it will likely have lower CPU overhead.  Note that it is CRITICALLY IMPORTANT to disassociate visual rendering (in the requestAnimationFrame loop) from the onaudioprocess function - you do NOT want to trigger a relayout from inside your audio handler, or it may glitch or cause other issues.

It's also hosted at https://webaudiodemos.appspot.com/volume-meter/.

Check it out, feel free to fork, submit pull requests, etc.  MIT-Licensed - party on.

-Chris
