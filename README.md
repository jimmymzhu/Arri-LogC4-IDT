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
- Place "Arri_LogC4.dctl" in the IDT subfolder.
- Start Resolve.

At start up, Resolve loads all the ACES DCTLs inside the "ACES Transforms/IDT" and "ACES Transforms/ODT" folders.

Baselight:
---
-  Navigate to the "colourspaces" folder for colour space transform files.  
    - MacOS: "~/Library/Application Support/FilmLight/etc/colourspaces"
    - Linux: "/usr/fl/etc/colourspaces"
- Place "ARRI_LogC4_WG4_full.flspace" in the "colourspaces" folder.
- Start Baselight.

OCIO:
---
- Open the ACES config folder on your local workstation
- add the config from Arri_LogC-config.ocio into config.ocio
- copy "V4_LogC_800_to_linear.spi1d" into the "luts" folder