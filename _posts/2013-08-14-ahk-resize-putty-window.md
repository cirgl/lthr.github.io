---
layout: post
title: Resize PuTTY window with AutoHotkey
tags:
- autohotkey
---

To resize a PuTTY window with AutoHotkey, to fx. 1000×500 px, i’m using this script.


	; Resize PuTTY window
	^1::
	    SetTitleMatchMode, 2
	    IfWinExist, ahk_class PuTTY
	    {
	        WinGetPos, x, y, w, h, PuTTY
	        WM_ENTERSIZEMOVE=0x0231
	        WM_EXITSIZEMOVE=0x0232
	        SendMessage, WM_ENTERSIZEMOVE
	        WinMove, , , , , 1000, 500
	        SendMessage, WM_EXITSIZEMOVE
	    }
	    Return
