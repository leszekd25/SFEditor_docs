# Heightmap editor mode
Terrain is built from a heightmap. This editor mode allows you to edit the heightmap and see the effects on terrain immediately.
## User interface

![enter image description here](https://lh3.googleusercontent.com/4ifb0GaiuIRSNGOFdZK284rGAuDAIiQ2yrCyzaZGV4JPMGyjAPfpdSbGsqcyx1XFBlAG4ibQeYMP)
1. Sculpt **brush**
2. Sculpt mode
3. Brush strength/value

### Sculpt brush
You use brush to paint on terrain - whether it's height paint, texture paint, or anything else.
#### Size
Radius of the brush. The larger the size, the bigger the area affected by brush.
#### Shape
Currently, brush supports 3 shapes: **Square**, **Circle**, **Diamond**. Circle is the default shape, and is usually enough for most cases.
#### Interpolation mode
There are 4 interpolation modes for painting brush, all of which affect relative strength of the brush in the painting area: **Constant**, **Linear**, **Square**, **Sinusoidal**.
![enter image description here](https://lh3.googleusercontent.com/XPk99Xk4gshGcijB1rENRPJOZqvjGnt0E2Lyr3L_ce6XQt5zczvMLRiHmYYEoo_XVlGOS3VuC4EY)
### Draw mode
Heightmap editor has 5 sculpt modes available to shape the terrain.
#### Add, Subtract
![enter image description here](https://lh3.googleusercontent.com/AT3ndLkEzVW_Q5VoKa2LBDEOMNR4khseva3r_EcXdNwmwnOva9MejhpNrcv6d67Ny7gdfIGY6zg-)
Add mode simply adds height to existing terrain. Subtract mode takes that height away.
Strength denotes the height displacement at the center of brush on a single stroke.
#### Set
![enter image description here](https://lh3.googleusercontent.com/v_8APW5IF6_EjHVvP7QDCXmGJWvP6chIANDsTQnoPdYigSBxFl_h05e2HspG9Bulyw0qckfm3a4E)
Set mode sets height at a desired value. Interpolation mode does not apply.
Value denotes the height the terrain will be set to.
#### Smooth
![enter image description here](https://lh3.googleusercontent.com/iQaTFjw1nJWE-4ziuMwHgJ6jowPQ_XgRqgtAaD4wbiQzGmsGdhDDFsXwS1yKGUI3GyYuBCq1kB8H)
Smooth mode smooths out terrain, diminishing irregularities.
Value denotes how much the terrain will be smoothed out in a single stroke, and should be a value between 0 and 100.
#### Rough
![enter image description here](https://lh3.googleusercontent.com/d2P7WxeekVCh2yZ-ED7xaDdMsWAPU-Z2rpmv6KL8GOfuyHcwp0Pcgd9ckoi9CwohB-fWF6P7CFXr)
Rough mode roughs up the terrain, attenuating irregularities.
Value denotes how much the terrain will be roughed up in a single stroke, and should be a value between 0 and 100.

## 3D display controls
You can use Left Mouse Button or Right Mouse Button to modify terrain.
- Add mode: LMB to add terrain, RMB to subtract terrain
- Subtract mode: LMB to subtract terrain, RMB to add terrain
- Set mode: LMB to set terrain, RMB to probe terrain (get height value)
- Smooth mode: LMB to smooth out terrain, RMB to rough it up
- Rough mode: LMB to rough up terrain, RMB to smooth it out


## Additional information
Editor Status shows terrain height at the 3D cursor position while you're in Heightmap editor mode.

Terrain height can't be lower than 0 or higher than 65535. Terrain with height 0 denotes area submerged in ocean and is **impassable**.

You can't modify terrain under a lake.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc3OTU3MDYyOF19
-->