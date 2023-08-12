---
authors: 
- "Matthew Lamont"
categories:
- Windows
date: "2017-01-09T15:53:21Z"
tags:
- Free Software
- Open Source
- Tutorials
- Windows 10
title: Fixing Graphic Errors in old DirectX using WineD3D
aliases:
  - /fixing-graphic-errors-in-old-directx-using-wined3d/
slug: /fixing-graphic-errors-in-old-directx-using-wined3d/
---

Many of us have old games laying around and realize that they just don't work right. This can be due to many issues, but today we will cover DirectX issues using WineD3D for Windows.

WineD3D for Windows is a "DirectX 1-11 to OpenGL wrapper based on WineD3D". Normally WineD3D is used to run DirectX games on Linux, but some old Windows games do not run on Windows anymore. Lets take Star Wars Battlefront 2 for example. On Windows 10, some maps have issues displaying the right colors. To fix this we will need a replacement for DirectX 9.

You can download [WineD3D for Windows here](https://fdossena.com/?p=wined3d/index.frag)

## Getting it Working

There is a readme in the zip folder that WineD3D come in. For Battlefront 2, we will copy the d3d9.dll, libwine.dll and wined3d.dll into the data directory that the game's executable is located. BattlefrontII.exe is located here.

When you load it up, the game works as it should.


The game should now run properly. This works with many games, but is not guaranteed.

WineD3D is far from perfect and has issues: Some games will not work, stutter, or lock to low resolutions. If you would like to help improve it, it is open source under the GNU LGPL Version 2.