# JG Maker R1 Printer

## Background / Preparing

- https://www.jgmaker3d.com/products/jg-maker-r1-3d-printer
- JGcreat 5.2.5 is the proprietary slicer from JGMaker (JGAurora) which can be obtained from https://www.jgmaker3d.com/pages/document-download. It is based on Ultimaker Cura and contains printer profiles for all the JG Maker printers. For example, the R1 profile was found at `JGcreat5.2.5\share\cura\resources\definitions\jgmaker_r-1.def.json` and contained start/end g-code, the print bed dimensions, etc. There were also speed/print height profiles in `JGcreat5.2.5\share\cura\resources\quality\jgmaker\jgmaker_r-1\jm_r-1_global_optimal.inst.cfg`
- The JGCreate profiles were opened up in Ultimaker Cura and input manually into a "Custom FFF Printer" in the "Add a Local Printer" section of Ultimaker Cura 5.11.0 https://ultimaker.com/software/ultimaker-cura/. Since both are based on Cura, the input boxes are largely similar
- The R1 profile was then manually input into PrusaSlicer 2.9.4. In the Add/Remove Presets (Configuration Wizard) there is a section for Custom Printer. The R1 printer profile can then be built from there. However, it will also need profiles to be built for filament and layer printing settings. Once the profile is functional, it can be exported with File -> Export -> Export Config Bundle. No need for the physical printers part as those are USB-connected printers, which is irrelevant here


## Importing to Your Slicer
- Cura offers a Help -> Show Configuration Folder shortcut. You can drop the folders and files in their respective locations in that directory while Cura is closed, and then Cura will open and recognize the new profiles
- PrusaSlicer offers a File -> Import -> Import Config Bundle option, where the single `PrusaSlicer_config_bundle.ini` file can be imported with all the settings relevant to the printer, extruder, filament, and more