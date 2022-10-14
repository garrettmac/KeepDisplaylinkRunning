# KeepDisplaylinkRunning

A LaunchAgent to keep DisplayLink always running. Useful for the first M1 Macbook Pros that dont support duel displays without this workaround.

I made a mod where I removed my broken screen on my M1 and I always need the DisplayLink App running, any time I would unplug the usb-c cord it would close the app so plugging it back in was a nightmare to get it up and running again.

![IMG_8901](https://user-images.githubusercontent.com/5916111/195893642-7efb02d3-5a3d-4738-8fea-2b97dd6f1a1c.jpeg)

## How install

### 1. Install DisplayLink for mac
https://www.synaptics.com/products/displaylink-graphics/downloads/macos


### 2. Add this keep live script to your LaunchAgents

```sh
git clone git@github.com:garrettmac/KeepDisplaylinkRunning.git
mv KeepDisplaylinkRunning/io.garrettmac.keep.displaylink.running.plist /Users/$(whoami)/Library/LaunchAgents/io.garrettmac.keep.displaylink.running.plist
launchctl load /Users/$(whoami)/Library/LaunchAgents/io.garrettmac.keep.displaylink.running.plist
```

or if you're not as techy savy...

Just add the `io.garrettmac.keep.displaylink.running.plist` file in your `/Users/[YOUR USERNAME HERE]/Library/LaunchAgents` directory and restart your computer
