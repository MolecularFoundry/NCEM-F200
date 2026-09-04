# NCEM JEOL JEM-F200 Operations and Alignment Manual

## 🛑 MODULE 1: Safety & Instrument Precautions

### 1.1 Column Vacuum Safety
*   **Critical Threshold:** Always monitor the column pressure via **SIP3** on the *Valve/Vacuum Monitor* window. **Never open the beam valves if SIP3 is above $4.0 \times 10^{-5}$ Pa**. Operating above this threshold risks severe column contamination or damage to the Schottky field emission source.
*   **ACD Liquid Nitrogen:** Before opening beam valves or running high-tension (HT) operations, ensure the Anti-Contamination Device (ACD) tank is properly cooled. Fill the ACD tank with liquid nitrogen ($LN_2$) and wait **15 minutes** for the initial refrigeration, then refill the tank. It takes approximately **1 hour** to fully refrigerate the ACD.

### 1.2 Cold Field Emission Gun (CFEG) Flashing Rules
*   **High Flash (Daily):** A **High Flash** must be performed once every **24 hours** (typically at the beginning of the day/morning) to clean the emitter tip and generate stable emission.
*   **Low Flash (During Sessions):** If the emission current drops below **$9\,\mu\text{A}$** during a user session, a **Low Flash** should be executed to restore emission current.
*   **Prerequisite:** The beam can only be generated and flashing performed if the specimen holder is fully inserted into the goniometer column.

### 1.3 Beryllium and Specimen Holder Hazards
*   **Double-Tilt EDS Holder Safety:** When handling Beryllium-containing holders (such as the Beryllium double-tilt EDS holder), prevent exposure to moisture or mechanical stress. 
*   **Cable Connection:** Before introducing the double-tilt holder into the column, ensure the TLT-Y beta tilt cable is properly plugged into the goniometer TL-Y / TLT-Y socket to avoid damage or sensor errors.

### 1.4 High-Tilt 3-Sample Holder Mechanical Collision Warning
*   ⚠️ **CRITICAL MECHANICAL HAZARD:** The high-tilt **3-sample holder** has a physical collision risk inside the column. **Position 3 on the 3-sample holder will physically collide with EDS Detector #2** when inserted.
*   **Safety Rule:** Never tilt or navigate to Position 3 without verifying that EDS Detector #2 is completely retracted to its home position.

### 1.5 FEMTUS EDS Cooling & S-CHANGE 1-Hour Timeout Safety
*   **The S-CHANGE Cooling Loop:** Clicking the **S-CHANGE** button on the detector controller retracts the EDS detector to its safe home position (most distant from the column) and initiates or continues detector cooling.
*   ⚠️ **AUTOMATIC TIMEOUT SAFETY HAZARD:** If you do not perform any microscope or software operation for **more than 1 hour** after clicking S-CHANGE, **the system automatically enters BAKE mode**.
*   **The Danger:** Transitioning to BAKE mode **automatically stops detector cooling**. This causes the EDS detector to warm up unexpectedly, which can degrade sensor performance or damage sensitive components if left unattended.
*   **Correction Step:** To resume cooling if the timeout occurs, you must click the **S-CHANGE button again**. Cooling takes about **3 minutes** before measurement can safely resume.

---

## 🛠️ MODULE 2: Standard User Workflows

### 2.1 CFEG Emission Ramping & Accelerating Voltage (HT) Switching
If the accelerating voltage (HT) is not set to your desired operating value (80kV or 200kV), use the following procedure:
1.  Click the **Vacuum: Ready** link in the *Detector/Aperture* window to open the *Valve/Vacuum Monitor*. Verify column pressure is safe.
2.  In the *TEM Center* panel, click the **HT** button.
3.  **For 80kV Operation:** Expand the menu and **turn on the EL short** by clicking **100**. (This protects the column and optimizes low-voltage optics).
4.  **For 200kV Operation:** Expand the menu and ensure the **EL short is turned OFF**.
5.  Select the desired target HT voltage (only **80kV** and **200kV** are available). The selected target will illuminate in **green**.
6.  Ensure the **HT ON** button is green; click it to ramp the voltage if it is not.
7.  Perform a CFEG **High Flash** (if first session of the day) or **Low Flash** (if emission current drops below $9\,\mu\text{A}$) to stabilize the beam.

### 2.2 Specimen Loading and Holder Insertion
#### Required Safety Precautions (Must check before ANY holder exchange):
1.  **Stage is in the neutral (zeroed) position.**
2.  **Beam valves are completely closed.**
3.  **All EDS detectors are fully retracted.**
4.  **Objective (HC) aperture is retracted.**
5.  **Dectris Arina camera is retracted AND its high voltage is turned OFF** (the lightning bolt icon in TVIPS software must show the word **"Off"** underneath).
6.  **ClearView Camera is retracted.**
7.  If utilizing the **3-sample holder**, navigate back to **Sample Position 1** before retraction.

#### Workflow A: Manual Insertion Procedure
1.  Verify the third button on the goniometer panel is set to **"Manual"**. If it displays "Auto," press it to toggle it back.
2.  Align the holder's mini pin with the groove at the **9 o'clock position** on the goniometer. Insert the holder until you reach a physical stop. **DO NOT ROTATE THE HOLDER YET**.
3.  Push the **"Air"** button on the goniometer panel. The display will toggle to **"Pump"** and flash. The mechanical roughing/diffusion pump will begin pumping out the specimen chamber.
4.  Monitor the pressure indicator **PiG4** in the *Valve/Vacuum Monitor* (accessed by clicking Vacuum Ready in the TEM schematic in TEM Center). Because valves **V8** and **V21** are open (green), PiG4 should begin dropping rapidly.
5.  **Insertion Phase:** Once PiG4 drops below **$36\,\mu\text{A}$**, you can insert the holder into the column by following this exact, careful mechanical sequence:
    *   **Step a:** Rotate the holder slightly clockwise until it hits a physical stop.
    *   **Step b:** Push the holder straight in slightly until it hits a stop.
    *   **Step c:** Rotate the holder a long clockwise turn until it reaches a physical stop.
    *   **Step d:** Gently guide the holder straight in for a long insertion until it is fully seated in the column.
6.  In the *Open Project* window, select the correct TEM holder configuration; this is required for the stage navigator (nanospace map) to function accurately.
7.  If utilizing a double-tilt holder, plug the tilt cable into the goniometer **TLT-Y** socket.

#### Workflow B: Automated Insertion and Retraction via SpecPorter : incomplete
*   **Preparation:** Ensure the goniometer cover is **fully opened** (the SpecPorter sequence will not initiate if the cover is partially closed).
*   **Execution:** Double-click the **Holder** icon on the screen interface. Ensure that **"Auto"** is active. The automated carrier plate replaces and seats the holder without operator intervention.
*   Select the correct holder, and make sure the holder icon indicates "Specporter OK". This procedure is currently incomplete and needs to be corrected. 
---

### 2.3 Basic TEM Mode Operations & Z-Height (Eucentric) Focus
1.  Open the beam valves by pressing the **BEAM** switch on the left-hand panel (or click the column schematic drawing in *TEM Center*).
2.  Select **Spot Size 1**, **Alpha 1** in TEM Mode.
3.  Click on the camera icon in the TEM Center software to view the live image. If you cannot find the beam, decrease magnification, switch to **Low Mag** mode, check specimen position, or retract apertures.
4.  **Z-Height Focus (Eucentric Height) Alignment:**
    *   Find a recognizable feature or particle on the specimen.
    *   Press the **STD FOCUS** button on the right-hand panel. This sets the standard focal length of the objective lens (OLF analog reference value is **1.88**).
    *   Activate the **IMAGE WOBB X** or **Y** wobbler on the left-hand panel to oscillate the beam.
    *   Focus the specimen by adjusting the stage physical height up or down using the **Z-height buttons** ($\\text{Z}\\blacktriangle$ and $\\text{Z}\\blacktriangledown$) on the stage rotation panel. Align the specimen height until the image vibration/wobble is completely minimized and the image merges into a single focused view.
    *   Disable the wobbler and perform fine focusing using the physical **OBJ FOCUS** knob on the right-hand panel.

---

### 2.4 Standard TEM Alignments (Linear Workflow)

#### A. CL (Condenser Lens) Aperture Centering
*   *Note: Standardize on physical **CL Aperture** designations (CL Aperture No. 1, 2, 3, or 4) rather than using C2 or condenser interchangeably.*
1.  Converge the beam into a small spot using the **BRIGHTNESS** knob.
2.  Center the spot on the screen using the physical **SHIFT X/Y** knobs.
3.  Select physical **CL Aperture No. 1 or No. 2** (used for TEM mode).
4.  Slowly turn the **BRIGHTNESS** knob clockwise to spread the beam. 
5.  If the beam spreads asymmetrically relative to the center of the screen, adjust the physical mechanical centering screws on the CL aperture drive until the beam expands and contracts perfectly concentrically about the screen center.
6.  Repeat this process (converge, center with shift knobs, spread, adjust mechanical screws) until the aperture is perfectly aligned.

#### B. Condenser Lens Stigmation (CL Stig)
1.  Choose your desired operating spot size (e.g., spot size 2 or 3 for high-resolution imaging).
2.  Converge the beam to a small crossover spot.
3.  Press the **CL STIG** (or **COND STIG**) assignment button on the left hand panel.
4.  Turn the **BRIGHTNESS** knob clockwise to spread the beam. 
5.  Observe the shape of the spread beam. If it is elliptical (astigmatic), use the physical **DEF/STIG X/Y** knobs to correct the astigmatism until the beam spreads into a perfect, uniform circle.

#### C. High-Tension (HT) Voltage Centering
*   *Note: This centers the voltage axis of the column to minimize chromatic aberration.*
1.  Set the microscope magnification to **100kX** (for coarse centering) or up to **250kX** (for accurate centering on a small particle).
2.  Focus the specimen features at eucentric height using the **Z-height** stage controls and the physical **OBJ FOCUS** knob after pressing **STD FOCUS**.
3.  Select the physical **BRIGHT TILT** button on the left hand panel.
4.  Converge the beam and center the bright crossover spot on the screen using the dedicated physical **SHIFT X/Y** knobs.
    *   🔑 **HW Control Principle:** The physical `SHIFT X/Y` knobs are hardwired, dedicated controls for **beam shift**. Selecting `BRIGHT TILT` or any other assignment reassigns the `DEF/STIG` knobs, but the `SHIFT` knobs continue to control beam shift directly without conflict. This allows you to shift the beam and adjust tilt simultaneously and efficiently.
5.  Turn the **BRIGHTNESS** knob clockwise to spread the beam slightly larger than the screen.
6.  Enable the **HT WOBBLE** switch in the *Wobbler* window of the software.
7.  While the beam is wobbling, use the physical **DEF/STIG X/Y** knobs (now mapped to beam tilt because `BRIGHT TILT` is active) to adjust the beam tilt until the image expands and contracts concentrically about the center of the screen without lateral shifting.
8.  Turn off the **HT WOBBLE** switch.
9.  Converge the beam back to crossover, and if it has drifted, center it on the screen using the dedicated **SHIFT X/Y** knobs.
10. Repeat steps 5 through 9 until there is zero lateral shifting when the HT wobble is active.

---

### 2.5 STEM Mode Transition & Ronchigram Alignment

#### A. Transitioning to STEM Mode
1.  While in TEM mode, converge the beam into a small crossover spot using the **BRIGHTNESS** knob.
2.  Ensure **BRIGHT TILT** is selected on the left hand panel.
3.  Center the spot to the exact center of the fluorescent screen using the physical **SHIFT X/Y** knobs.
4.  In the *TEM Center* software interface, navigate to the *Detector/Aperture* panel, open the *Operation Mode* setting, and select **Scanning**. The lens settings will automatically configure for STEM scanning.

#### B. Ronchigram Alignment & Probe Tuning
1.  In the *Scan* tab of *TEM Center*, ensure you are in **Spot Mode** to park the beam in a single location.
2.  Press the **Ronchigram** button under the *Scan* menu panel to display the shadow image on the fluorescent screen camera.
3.  Select a Camera Length of **1000 mm or higher** (e.g., 1000mm) so the Ronchigram details can be clearly resolved.
4.  Move the stage to position an amorphous region of your specimen (such as carbon support film) directly under the beam.
5.  Double-click the **STD FOCUS** button on the right hand panel to set the objective lens to its default STEM focus.
6.  Focus the Ronchigram by adjusting the stage physical **Z-height** up or down until you see the shadow image features expand. Continue to adjust Z-height until the "magnification" of the amorphous shadow image becomes nearly infinite, displaying a flat, uniform, and featureless central region (the center of convergence/divergence).
7.  **Correct 2-Fold Astigmatism:** Click the **CL STIG** (or **COND STIG**) button on the left hand panel. Use the physical **DEF/STIG X/Y** knobs to correct the astigmatism in the Ronchigram, turning the elliptical distortion into a perfectly circular, concentric pattern.
8.  **OBJ Wobbler Rotation Center (Rarely Needed):** If needed, activate the **OL wobble** in the *Wobbler* window of the *Lens/Deflector* tab. Ensure the center of the uniform, flat Ronchigram region remains the stationary center of the convergence/divergence wobble. If it is shifting, select **BRIGHT TILT** and adjust the physical **DEF/STIG** knobs until it is stationary. Disable the OL wobble when complete.
9.  **PLA Centering:** Turn on the Projector Lens Alignment (**PLA**) button on the left hand panel. Use the physical **DEF/STIG X/Y** knobs to center the flat, uniform central part of the Ronchigram precisely on the crosshairs of the screen camera. Disable PLA when finished.
10. **Insert CL Aperture No. 3:** Physical **CL Aperture No. 3** (typically $40\,\mu\text{m}$) is standard for STEM imaging. Insert the aperture and mechanically center it concentrically around the flat, aligned region of the Ronchigram.
11. **Final STEM Setup:** Disable the Ronchigram mode. Change the Camera Length to **200 mm or 300 mm** (ideal for Dark Field STEM imaging). In the *Scan* menu, select **Full Scan** (or disable Spot mode) to initiate active raster scanning. Ensure **Scan DFI Upper** is active in the *View* panel to view the High-Angle Annular Dark Field (HAADF) image.

---

### 2.6 Specialized Acquisitions

#### A. EDS Spectra and Mapping Acquisition (FEMTUS)
1.  **Detector Retraction & Cooling:** Click the **S-CHANGE** button on the detector controller. This retracts the detector safely and initiates cooling. Wait at least **3 minutes** for the cooling cycle to complete. Ensure you do not leave the system in S-CHANGE mode unattended for over 1 hour to prevent the auto-timeout bake hazard.
2.  **Double Check Specimen Position:** Verify that you are **NOT in Position 3** if utilizing the high-tilt 3-sample holder, to prevent a critical physical collision with EDS Detector #2.
3.  **Detector Insertion:** Click the **INSERT** button on the detector controller. The physical detector will move into its close-in analysis position.
4.  **Process Time Selection:** Select the desired Process Time (T1 through T5) depending on your experimental needs (T1 is optimized for fast mapping/high count rates; T5 is optimized for high energy resolution).
5.  Acquire your spectra or maps. Once complete, click **BAKE** or **S-CHANGE** to safely retract the detector and preserve the cooling state.

#### B. 4D-STEM Data Collection (Dectris Arina Camera & TVIPS Scan Generator)
1.  Align the TEM column in micro-diffraction (**uDiff**) or standard STEM diffraction mode. Set your desired convergence angle, CL aperture, and spot size.
2.  **Camera Conflict Check (Crucial):** The TVIPS ClearView and Dectris Arina cameras sit on the same physical plane. **Verify that the ClearView camera is completely retracted before attempting to insert the Arina camera**.
3.  **Aperture & Scan Setup:** Switch the physical external scanning coils from Gatan control to Dectris control. Set the scan switch box to **EDS 2**.
4.  **Insert the Arina Camera:** Push the appropriate insertion button on the retro silver triangular console (positioned under the Gatan monitors on the F200 desk). The indicator lights will illuminate once the camera is fully inserted.
5.  **Detector High Voltage Safety:** In the TVIPS *Emplified Scan* software, navigate to the *Dectris* tab and click on the **lightning bolt** icon to turn ON the detector high-voltage.
    *   ⚠️ **HIGH VOLTAGE SAFETY RULE:** **Always turn the Arina detector voltage OFF** (the lightning bolt icon must display "Off") when the detector is not actively acquiring data, or whenever you are opening/closing the column beam valves.
6.  **Retract Fluorescent Screen:** Retract the physical fluorescent screen and the standard STEM Bright Field (BF) detector to clear the path to the Arina sensor.
7.  Once the detector voltage is ready (the lightning bolt shows "Ready"), select **Continuous** in the *Scan* tab to view the live diffraction pattern. 
8.  Use **PLA** with the physical **DEF/STIG** knobs to center the diffraction beam on the Arina camera sensor. You can adjust Camera Length or zoom in/out with the mouse scroll wheel.
9.  **Collect Data:** Execute your 4D-STEM raster scan. Once acquisition is complete, click **Abort**, turn the Arina detector high voltage **OFF**, and retract the camera.

---

### 2.7 End-of-Session & Shutdown Procedures
1.  Close the column beam valves (the **BEAM** switch on the hand panel should be unlit).
2.  Retract the specimen holder from the column (using Manual or automated SpecPorter retraction workflows).
3.  Ensure all physical apertures (Objective/HC, SAD, CL) and the EDS detectors are fully retracted.
4.  **ACD Heat Cycle (Daily Shutdown):**
    *   Ensure the specimen holder has been completely removed from the goniometer column.
    *   Confirm all column valves are closed.
    *   Insert the physical dry-nitrogen gas warming heater into the ACD cold trap tank.
    *   In the vacuum software interface, click the **Start** button under the *ACD Heat* cycle menu. This initiates an automated **8-hour heating bake** to warm the cold trap and purge accumulated moisture, preparing the column vacuum for the next day's operation.

---

## 🔬 MODULE 3: Staff-Only Maintenance & Calibration

### 3.1 Gun Shift and Gun Tilt Alignment
*   *Note: This alignment matches the electron gun source trajectory to the optical axis across different condenser lens currents. It should be performed weekly by qualified staff.*
1.  Set the microscope magnification to **40kX**.
2.  Select **Bright Tilt** on the left hand panel.
3.  Set the Spot Size to **5**.
4.  Converge the beam to a crossover spot using the **BRIGHTNESS** knob, and center it precisely on the screen using the dedicated physical **SHIFT X/Y** knobs.
5.  Switch the Spot Size to **1**.
6.  Open the software alignment panel and click the **GUN** alignment option.
7.  Converge the beam and use the physical **SHIFT X/Y** knobs to re-center the crossover spot on the screen.
8.  Toggle the Spot Size back to **5**.
9.  Select **Bright Tilt** and use the physical **DEF/STIG X/Y** knobs (which now control gun tilt) to align the converged beam.
10. Repeat steps 4 through 9 iteratively until the converged beam crossover spot remains stationary on the screen when switching back and forth between Spot Size 1 and Spot Size 5.
11. *Note:* Gun alignments for each accelerating voltage angle value are completely independent and can be performed individually at angles 1 through 5.

### 3.2 Pivot Point Calibration (Tilt/Shift Balance)
*   *Note: This decoupling calibration ensures that tilting the beam (BRIGHT TILT) does not introduce lateral beam shift, and shifting the beam does not introduce beam tilt. This calibration is done rarely.*
1.  Set the microscope magnification to **40kX**. *(Note: Corrected from the '40kV' typographical error in older drafts).*
2.  Converge the beam to a crossover spot using the **BRIGHTNESS** knob.
3.  Open the software *Wobbler* window and turn on the **Wobbler Tilt X**.
4.  Observe the converged spot. If the spot vibrates or moves laterally on the screen, use the physical **DEF/STIG X/Y** knobs to adjust the compensator alignment until the lateral movement is eliminated and the spot only "breathes" or tilts in place.
    *   *Troubleshooting:* If turning on Wobbler Tilt X causes lateral movement in the perpendicular Y direction, you may need to adjust the **CL Compe Angle** setting in the alignment register.
5.  Disable Wobbler Tilt X, and enable **Wobbler Tilt Y**. Repeat the adjustment using the DEF/STIG knobs until lateral shifting is eliminated.
6.  **Shift Balance Calibration:** Enable the **Wobbler Shift X**. Use the physical **DEF/STIG** knobs to eliminate any lateral shifting. Repeat the process for **Wobbler Shift Y**.
7.  Iterate back and complete a final **HT Voltage Centering** check to ensure the optical axes converge.

### 3.3 Intermediate Lens Stigmation (SA Diffraction Caustic Calibration)
*   *Note: This alignment corrects intermediate lens astigmatism to ensure diffraction spots and polycrystalline diffraction rings are perfectly round.*
1.  Select **SA DIFF** mode on the left-hand panel.
2.  Set the Camera Length to **200 cm**.
3.  Turn the physical **BRIGHTNESS** knob fully clockwise.
4.  Focus the beam using the **DIFF FOCUS** knob until you obtain a sharp, high-intensity **caustic spot** on the screen.
5.  Select **PLA** (Projector Lens Alignment) on the left hand panel and use the physical **DEF/STIG** knobs to position the caustic spot exactly in the center of the screen.
6.  Open the *Lens/Deflector* window. Move the mouse pointer over the **IL Stig** label, and click the **Assign to knobs** button. (This maps the physical hand panel knobs to the intermediate lens stigmators).
7.  Enable the physical **IL STIG** button on the left hand panel.
8.  Observe the caustic spot shape. Adjust the physical **DEF/STIG X/Y** knobs until the astigmatism is corrected and you obtain a perfectly symmetrical, **3-fold symmetric caustic spot** on the screen.
9.  Disable **IL STIG** and **PLA** when finished.
