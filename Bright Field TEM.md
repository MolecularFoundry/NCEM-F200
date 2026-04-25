# Basic TEM Alignment Procedures

## Start Viewing
1. If column vacuum is below 4E-5Pa, press the beam button to open the column valve. 
2. Click on "Cam" in the TEM Center to see the fluorescent screen camera image. 
3. Insert a C2 aperture and center it.
4. Go to Spot 1, Alpha 1. 
5. Push the std focus button. 
6. View the image on the fluorescent screen and bring the image into focus using Z height. You can use the image wobbler to make this easier. 

## Aligning the Column
1. Picking the Spot and Angle number : The spot (1-5) moves the crossover between the gun and C1 lens, and is used to adjust the beam current. The angle selector move the crossover between C3 and C-mini lens, which decides at what magnification you can have parallel illumination. 

If you select the button "Convergent Mag Link" and "Brightness Mag Link", F2 will automatically change Angle dedending on illumination conditions.

| Angle | Magnification Range |
|-------|:-------------------:|
| 1     | > 300kX             |
| 2     | 80kX - 250kX        |
| 3     | 30kX - 60kX         |
| 4     | 5kX - 25kX          |
| 5     | <4kX                |

However, if your desired conditions do not give you a visible beam on the screen, and your sample is not blocking the beam, you can move to a smaller spot size number (larger beam current). 

2. Press the standard focus button, and adjust [Z height](Z height.md). 
3. Insert the largest C2 aperture and [center it](Centering C2 Aperture.md).
4. Adjust Condenser Stigmation by clicking the Cond Stig button on the left hand panel, and using the DEF/STIG buttons on the left and right hand panels. Make the illuminated area as round as possible on either side of crossover. If this alignment is not looking OK, do the best you can and revsiit this after adjusting the voltage center. 
5. Follow the procedure for [voltage centering](Voltage Centering.md).
6. Follow the procedure for [condenser stigmation](Condenser Stigmation.md).
   
## Objective stigmation
This alignment is needed hor high resolution TEM and needs a reasonably thin amorphous specimen. The stage should also not be drifting too much and the sample should be stable under electron beam radiation. The workflow involves imaging the amorphous specimen on a camera, and make sure the fourier transform of the image has rotational symmetry. 

1. Find a suitable amorphous region.
2. Set the magnification to ~ 300 to 600kX.
3. Image the specimen on the clearview camera, and under start a live FFT in GMS by navigating to process-> life->FFT.
4. Change the defocus till you see 2-3 orders of rings in the FFT.
5. Select the OBJ STIG button on the left hand panel, and adjust the DEF/STIG knobs till the rings are circular. You can make a ellicptial annotation on the FFT and hold down the shift key while making the annotation. This will force the ellipse to be circular and this circle can serve as a guide to judge ellipticity of the FFT. 
6. Adjust the defocus such that you see only 1 ring in the FFT and adjust objective stigmation if needed. 

## Aligning the Objective aperture for BF/DF

This alignment is only needed if you want to do high contrast TEM. Inserting an objective aperture will cut off the electrons scattered to high angles, which contain the high spatial frequency information needed to reconstrust an atomic resolution TEM image. However, for  BF/DF imaging where diffraction contrast needs to be maximized, this is very useful. 

1. Insert an appropritate SAD aperture. 
2. Select SA DIFF by pushing the DIFF button on the right hand console. 
3. Insert an objective (HC) aperture.
4. Sharpen the direct beam with the brightness knob-- this is essentially making sure your beam is parallel and not convergent or divergent. 
5. Make sure the edge of the inserted aperture is in sharp focus by adjusting the IMAGE/DIFF FOCUS knob on the right hand panel. This controls the diffraction lens. 
6. Move the HC aperture so that it is centered around the direct beam. If you want to do dirty dark field imaging, move the HC aperture till it is positioned around a specific Bragg reflection. 
7. Return to MAG mode and retract the SAD aperture. You now have a bright field image or a dirty dark field image of your sample.
8. While imaging a DF image, you will likely need large binning and long exposure times.  

## HRTEM
Do all the alignments in the above sections, but work at spot 2 or 3, alpha 1, and at a high magnification of 400kX. 

## Dark Field TEM
1. Align the optical axis as described above. 
2. Focus on the sample.
3. Confirm [voltage center](Voltage Centering.md).
4. Insert a SAD aperture, select DIFF on the right hand panel, and center the diffraction pattern using PLA on the left hand panel and adjusting the DEF/STIG knobs. 
5. Select Dark Tilt and center the direct beam using DEF/STIG.
6. Select Bright Tilt and center the direct beam using DEF/STIG. 
7. Repeat 5-6 till the diffraction pattern does not move as you toggle between bright tilt and dark tilt. This invariably will introduce some beam tilt into the column. 
8. While in DIFF mode, insert a small HC aperture. Focus on the edge of the aperture using the focus knob on the right hand panel, and sharpen the central spot using the brightness knob on the left hand panel. Once this is done, you have a parallel beam, so do not change brightness. 
9. Retract the HC aperture. 
10. Select dark tilt, and use the DEF/STIG knobs to center the desired diffraction spot. 
11. Insert the HC aperture and center it. 
12. Switch to MAG mode and retract the SAD aperture. 
13. Focus and record.

PS-- you can also tilt the stage in addition to the beam to use 2-beam imaging. 

