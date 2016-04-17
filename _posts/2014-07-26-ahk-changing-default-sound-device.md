---
layout: post
title: AHK - Changing the default sound device
tags:
- autohotkey
---

If you’re the kind of person who always have your headset connected to your computer, but still need to switch to PC speakers from time to time, here’s a little AutoHotkey-script that will switch the default sound device between those two.

What the script does is to open your Sound / Playback preferences window, select between the two options you’ve chosen, and set this as default. To give you an idea, look at my Playback preferences:

![](/public/sound.png)

In this case I’m switching between 1 (Speakers) and 2 (Speakers / HP). You need to change these numbers in the script, line 5, 7 and 16 (or delete line 16 if you prefer), if your Playback devices are set up different than mine. The script uses the keys <kbd>Ctrl</kbd>&nbsp;+&nbsp;<kbd>Win</kbd>&nbsp;+&nbsp;<kbd>F1</kbd> as default.

	; toggle speaker setup
	^#F1::
	    switch := !switch
	    If (switch)
	        usePlaybackDevice(1)
	    else
	        usePlaybackDevice(2)
	    return
	 
	usePlaybackDevice(device) {
	    Run, mmsys.cpl
	    WinWaitActive, Sound ahk_class #32770
	    ControlSend, SysListView321,{Down %device%}, Sound ahk_class #32770
	    ControlClick, Button2, Sound ahk_class #32770
	    WinClose, Sound ahk_class #32770
	    TrayTip, , % if device = 1 ? "Headset" : "PC speakers"
	}
