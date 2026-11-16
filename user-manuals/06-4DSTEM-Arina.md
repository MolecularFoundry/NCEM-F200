# 4D-STEM Data collection 

# Important safety notes! 
1. The ClearView and Arina cameras are at the same plane. Do not insert the Arina camera unless you are sure that the ClearView camera is retracted 
2. Turn the Arina detector high voltage off when not in use or opening/closing the beam valves. The lightning icon in TVIPS Emplified Scan software should have the word "Off" under it. 

# Specs
The frame rate is up to 120kHz (8.33 microseconds) at 96x96 and up to 30kHz (33.3 microscections) for 192x192.  2Kx2K scan positions is possible, typically 1Kx1K is max. This is a silicon chip. 

# Start-up
1. Align the TEM column in uuDiff mode. Select the appropriate convergence angle, C2 aperture and spot size for your experiment. 
2. Switch the external scan coils from Gatan to Dectris if you have not already done so. Change the Scan SW Box to EDS 2.
3. When you are sure that ClearView is retracted, you can insert the Arina camera. Use the retro silver triangular console with 3 big buttons under the Gatan monitors on the F200 desk. The indicator lights will show you when the camera in inserted or retracted.
4. The Arina camera has 3 tabs at the top: `Scan`, `Microscope`, and `Dectris`. We will start in the `Dectris` tab. 
5. Click on the lightning bolt to turn on the detector voltage. Regarding safety note #2, this is the voltage you need to turn on and off every time you open and close the beam valves or stop taking data. 
6. Retract the flu screen, the STEM BF detector.
7. Once the voltage has turned on, the ligtning icon will have the word "Ready" under it. You can view your diffration data by clicking `Continuous` under the `Scan` tab. This is a good place to use PLA to center your beam and to change camera length if needed. Usually it is helpful to start with the beam in spot mode (in TEM Center, under Scan tab) parked in the middle to center. Sometimes, it is helpful to leave scanning on if you're worried about descan for a low mag scan. Depending on your camera length, you may notice the HAADF blocking the edge of the camera. This is usually retracted for 4D-STEM. You can also zoom in on the detector with the middle scroll wheel. When you're happy with your alignment, click `Abort`.


# Acquiring data 
1. In the `Dectris` tab, make sure `File Writer` and `Autocopy` are on (highlighted in blue).
2. Move to the `Scan` tab. 
3. On the left panel, under scan configuration, you can set your dwell time and number of pixels. The colored boxes indicate different virtual images that are generated during the scan. It is recommended to have saving for those on (`Save images` must be blue) to make sure your metadata is saved. 
4. Set-up naming for your scans. On the top menu bar you can set directory and base file name. It is recommended to include ` %00%` at the end of your base file name. This is will number scans as acquired. 
5. Make sure you are in Full Scan mode in TEM Center. Under the `Scan` tab, click `Single` and this will acquire a dataset stored in a HDF5 file.  Again, it is recommended to remove the HAADF, however, if you do that, the live HAADF image will show no signal.
6. Bonus: by default, dectris sets the neutral position to be the middle of the field of view which can leave a burn mark. If you click on the small triangle under `Scan Control` you can adjust the neutral x and y in the `Scan Control` menu. 20,000 is a sensible value here.

# Checking data
1. After data is acquired you can view the data in Novena. 
2. Novena let's you view individual diffraction patterns, make virtual images, make mean diffraction patterns, and perform basic DPC/COM reconstructions. 
3. First you need to select your data. On the left menu bar, click on the three dots to select your master file.  If a file is already oepn, you need to click on the `close` button.
4. Right away, you'll be able to view individual patterns by dragging around the yellow spot.
5. Any further analysis required loading the data. Click `Preprocess` to load the data. 
6. In general, the next step is highlighted in yellow.

# Shut down
1. Turn off voltage on camera. If it won't let you click this button, restart EMplified. 
2. Retract camera 