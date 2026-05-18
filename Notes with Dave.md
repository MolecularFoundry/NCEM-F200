# 200 kV TEM Alignment Procedure

## Misc notes
- We dont have an objective aperture at the back focal place. We have a HC aperture outside the pole piece.
- Stigmation is different for every spot size.
- OLF is standard focus of 1.88 in "Analog" display. 
- They never touch beam shift in engineering mode because -- must keep beam shift at 8000 in engineering mode. 
- In STEM mode, do not change engineering mode settings. 
- Keep mag link off when doing aligments... only a convenience setting. 
- Users should not do image shifts, but wthe purposed of image shift 1 and 2 is the make sure the object doesnt move out of the middle as you cross mag ranges. 

Dave starts with no aperture, find a beam. 
Keep at std focus.

## Gun tilt and gun shift 
Not needed most times. 

##  C2 aperture Centering - do this first. 
Converge the beam, and center the bright dot with beam shift. 
Spread the aperture clockwise and center the aperture so that it is well centerd. 
Go to std focus

## Find Z ht
Can use image wobbler

## Anode wobbler
The moment you click anode wobbler, it will select gun align deflector. This may move the bright crossover dot away from the middle of the halo. 

## Gun / Condensor aligments:
Spot 1, gun shift, spot 5 beam shift. 

## HT Center

For rough alignment -> focus the converged spot at 40kX and make sure it is not moving.
For accurate aligment -> go to 250kX, spread the beam so you dont see the edges, and find a particle. Make sure it doesnt move. 

## Tilt Balance
Tilt X wobbler-- only look at the bright converged spot.

You may need to check CL Compe Angle if with Tilt X wobble, there is movememnt in Y . 
## Iterate back to HT Center


## Diff focus
- Spread beam to max
- Go to diff
- Max camL
- Adjust diff focus to make the smallest visible spot. May need to PLA to center. 

## Shift balance
Click the Shift X , adjust DEF/STIG, repeat for shift Y. 

## IL Stig
May be needed if diffraction is not well focused. Make polycrystalline rings round. 

## Spot Align
Only for keeping all the spots together when you change spot size. Never do this in STEM mode. 





## Alignment files
These files include the alignment saved in **engineering mode + any offsets done by the user at every kV in every mode**. So, reloading the saved aligment file will not reset scope, but if I back up a file -- that should reset all lenses and stigmators. Apertures are not saved in aligment files. These aperture locations are saved somewhere unclear, likely on a board memory. Even when users use the aperture positioning buttons, they are updating the saved memory.

## Mag Ranges

in M3, Image Shift 1 and 2, and PLA should be 8000
These change as you change Mag
M1 :  <4kX
M2 : 5kX - 30kX
M3 : 40kX - 1.2Mx
M4 : >1.5Mx

These mag ranges depend on pole piece. 

Image shift 1 and 2 are used to compensate shifts between mag ranges and between diff and mag. This should be done in engineer mode. 

## Mechanical Adjustments : we will never do this
Post specimen, IL is above PL. They go camL max and adjust IL1, and then go to camL min and adjust the lowest screws. 

Similar mechanical adjustment is pre-specimen. This is to make sure beam goes through center of CM (which is only there to make a paralllel beam. In TEM it is strongly focused and in STEM or probe mode the CM is almost off. The more convergent the beam, the weaker the CM value is).


## STEM Mode (Engineering mode)
- In engineering mode, spot 8, alpha 1.
- Move to spot 10, and the procedure says you need to drop the OLF by 0.01, so now it is 1.87
- CL3 was adjusted at spot 10 to get a rochigram to match the 40um aperture. 
- Then at all different spot sizes (called probe size in STEM), you adjust focus of the STEM image using CL2 in engineering mode. f 