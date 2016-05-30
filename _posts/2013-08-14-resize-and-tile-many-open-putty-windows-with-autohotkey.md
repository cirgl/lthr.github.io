---
layout: post
title: Resize and tile many open PuTTY windows with AutoHotkey
tags:
- autohotkey
---

To resize and tile many open PuTTY windows with AutoHotkey, i’m using this script.


    ; Tile PuTTY windows
    ^1::
        WinGetPos,,, desk_width, desk_height, Program Manager
        numberOfScreens := 2
        desk_width := desk_width / numberOfScreens
        desk_height := desk_height-30
        maxPuttyWinsX := 3
        maxPuttyWinsY := 3
        puttyWidth := desk_width/maxPuttyWinsX
        puttyHeight := desk_height/maxPuttyWinsY
     
        SetTitleMatchMode, 2
        IfWinExist, ahk_class PuTTY
        {
            yPos := 0
            xPos := 0
            yCount := 0
            Winget windows, list
            loop, %windows%
            {
                id := windows%A_Index%
                WinGetClass, winclass, ahk_id %id%
                if (InStr(winclass, "PuTTY"))
                {
                    WinActivate, ahk_id %id%
                    WM_ENTERSIZEMOVE=0x0231
                    WM_EXITSIZEMOVE=0x0232
                    SendMessage, WM_ENTERSIZEMOVE , 0, 0,, ahk_id %id%
                    WinMove, ahk_id %id% , , xPos, yPos, puttyWidth, puttyHeight
                    SendMessage, WM_EXITSIZEMOVE
                    yCount++
                    yPos := yPos + puttyHeight
                    if (yCount >= maxPuttyWinsY)
                    {
                        xPos := xPos + puttyWidth
                        yPos := 0
                        yCount := 0
                    }
                }
            }
        }
        return


Here’s an example of a 3×3 tile (set by maxPuttyWinsX and maxPuttyWinsY):

![PuTTY windows](/public/ahk-resize-many-windows.png)

The hotkey also activates the windows, which brings them all to front.
