---
layout: post
title: Open highlighted text in Google with AutoHotkey
tags:
- autohotkey
---

I often found myself highlighting text, copying it, opening a browser, and paste it into Google to search for it. Quite a few steps for such a small job i recon. I still have to highlight the text i’m interested in, but afterwards a shortcut <kbd>Ctrl</kbd> + <kbd>Win</kbd> + <kbd>G</kbd> does the rest of the job. This little addition to my AutoHotkey file save me quite some time in the long run.

	; Google search highlighted text
	^#g::
		Send, ^c
		Sleep 50
		Run, http://www.google.com/search?q=%clipboard%
		Return

Related to this, i’ve also begun to use <kbd>Ctrl</kbd> + <kbd>Win</kbd> + <kbd>W</kbd> to look up things on Wikipedia.

	; Wikipedia search highlighted text
	^#w::
	    Send, ^c
	    Sleep 50
	    Run, http://en.wikipedia.org/wiki/Special:Search?search=%clipboard%&go=Go
	    Return

The same principle can be used for dictionary sites, Google Translate, searching eBay, and so on. The only limit is the keyboard.
