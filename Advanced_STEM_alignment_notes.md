#Detailed STEM alignment notes

Written with Shane 17 June 2026
Updated with Kevin 7 July 2026

The `alignment` is very rarely used. The `OL wobbler` is more frequently used but still very occassionally. 

## Mag alignments can be done in `Alignment` (This is one of the four options in STEM for modes. The others are mag, low mag, and micro micro diff)
- This is the only place where you can tune CL3 to see the caustic spot. You can even take the aperature out to see the whole beam. This does not need to be done regularly.
- If the caustic spot isn't visible, you need to adjust focus.
- Here you can use the spot align x and y to center the bright spot. 
- Here you can use bright tilt to center the caustic spot in the shadow.

## OL, shift, and tilt wobbler
- This can be done in micro micro diff or mag mode. This is meant to be done on an amorphous sample. This alignment is specified in the JEOL manual on page 101 but not in much detail. 
- When you turn on the OL wobbler, beam align 2 is beam tilt, beam align1 is beam shift. Generally you don't want to mess with beam shift. We use beam tilt to center the expansion and minimize movement.
- In real space, scan across a field of view at low mag such as 25kx, if you click the tilt x and tilt y wobblers, you can adjust the CL Comp Tilt to minimize movement of the image. 
- In ronchigram mode, if you turn on shift x and shift y wobbler, you want to minimize movement of aperature. Switch back and forth between x and y as needed. This alignment should be done at high mag (800kx or higher)
- Iterate through these alignments as needed.


## Miscellaneous notes  
- IL stig is used for diffraction roundness. However, you probably don't need to do this alignment, so check other things first. 
- Alignments don't transfer between modes. For example, if you change bright tilt in mag, it doesn't necessarily transfter to micro micro diff. 
- We don't tune coma directly in STEM.
- You can set up multiple configurations of the funciton keys in case users want different defaults.
- OL stig doesn't do anything in STEM mode we think. 
- Anytime you're using a wobbler in STEM mode, you need to turn the amplitude down. STEM is more sensitive than TEM.
- Beam tilt is the same as bright tilt. Beam shift is the same function as spot align but used differently. Beam shift is separate deflectors, located in a similar part of the column. Spot align is the primary alignment and beam shift sits on top of that.





