# Arri LogC4 ACES IDT
Arri LogC4 IDT for Davinci Resolve, Baselight & OCIO

Based on https://www.arri.com/resource/blob/278790/bea879ac0d041a925bed27a096ab3ec2/2022-05-arri-logc4-specification-data.pdf

by Jimmy Zhu, www.jimmyzhu.net


Davinci Resolve:
---
- Navigate to the "ACES Transforms" folder in Resolve's main application support folder.
    - MacOS: "~/Library/Application Support/Blackmagic Design/DaVinci Resolve/ACES Transforms"   double check folders again
    - Windows: "%AppData%\Blackmagic Design\\DaVinci Resolve\\Support\\ACES Transforms"
    - Linux: "~/.local/share/DaVinciResolve/ACES Transforms"
- Place [Arri_LogC4.dctl](Davinci%20Resolve/Arri_LogC4.dctl) in the IDT subfolder.
- Start Resolve.
- At start up, Resolve loads all the ACES DCTLs inside the "ACES Transforms/IDT" and "ACES Transforms/ODT" folders.
- Arri LogC4 is now available as the ACES Input Transform in the project color management setting.
- Arri LogC4 is also available in the drop-down menu if you prefer a node tree based ACES workflow

Baselight:
---
-  Navigate to the "colourspaces" folder for colour space transform files.  
    - MacOS: "~/Library/Application Support/FilmLight/etc/colourspaces"
    - Linux: "/usr/fl/etc/colourspaces"
- Place [ARRI_LogC4_WG4_full.flspace](Baselight/ARRI_LogC4_WG4_full.flspace) in the "colourspaces" folder.
- Start Baselight.
- Arri: LogC4 / Wide Gamut4 is available for Colour Space Input.


OCIO:
---
- This config only contains the code for ARRI LogC4. If you don't have a full ACES OCIO config, you can download the latest ACES 1.2 OpenColorIO configuration files
- add the text from [Arri_LogC4-config.ocio](OCIO/Arri-LogC4-config.ocio) into full ACES config.ocio file
- copy [V4_LogC_800_to_linear.spi1d](OCIO/luts/V4_LogC_800_to_linear.spi1d) into the "luts" folder
- Load the modified OCIO config in DCC applications
- Input - ARRI - V4 LogC (EI800) - Wide Gamut is now available in OCIO
