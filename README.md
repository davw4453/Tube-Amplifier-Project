# Tube-Amplifier-Project
This is a vacuum tube amplifier with modular input modules to provide for different audio source methods. This project was designed for my captsone project at CCSU.

# Design Requirements 
The design requirement files created as part of the CCSU capstone program are under the DesignRequirementDocs directory. The overall requirements definition is in RequirementsDefinition_DavidWrinn.odt. Each individual module of the system is defined in their respective hardware component specification file. 

# CAUTION
This project uses non-isolated high-voltage US mains power (120V). Be careful of electric shock when constructing and servicing. 

# Build Procedure
These are the steps to construct the project.

1. Have the mainboard and aux input module manufactured at your fab house of choice (JLCPCB, OshPark, etc.).

Mainboard Gerbers: EDAFiles/KiCAD_SCH/tubeAmp/gerbers/
Aux Module Gerbers: EDAFiles/KiCAD_SCH/auxModule/auxModule/gerbers/

2. Assemble the PCBs according to the component designators in the BOM: BOM/tubeAmp_BOM.ods

3. 3D print the case and lid. You can load tubecase.stl and tubecase-lid.3MF into a slicer and print in the material of choice. (I used BambuStudio and printed in clear PLA). The .3mf files are the BambuStudio project files. The .sldprt and .slddrw files are Solidworks CAD files as that is what application I used to design the case and lid. 

4. Mount the boards and components into the case. The mainboard is mounted on M3 standoffs with M3 screws. The lid also uses M3 screws. The speakers are affixed with M4-.70 x 16 screws. The input module should slice in place from the side.

5. Insert a 1A fuse into the power jack, plug in, and enjoy.

Pictures for reference can be found in the Pictures directory. 

# Problems 

- A list of problems can be found in problems.txt.
- Due to inrush current, I had to put an ICL thermistor inline from the main wall supply before the 170VDC rectifier. The part I used was: Vishay Ametherm SL1522102. https://www.digikey.com/en/products/detail/vishay-ametherm/SL1522102/1873476?s=N4IgTCBcDaIKwHYAMBaAygGQIxzGLSYKAcgCIgC6AvkA 
- In a future revision I hope to increase the supply voltage from 170VDC to 300VDC to allow for more power output. 


© 2026 David Wrinn. This work is licensed under CC BY-NC-SA 4.0
