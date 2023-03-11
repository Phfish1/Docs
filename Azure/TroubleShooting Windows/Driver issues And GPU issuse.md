### General tips

- Reinstall, Update or downgrade your display driver. [Nvidia-Link](https://www.nvidia.com/Download/Find.aspx?lang=en-us) 

### Advances Tools

DDU ( Display Driver Uninstaller ) [LINK](https://www.guru3d.com/files-details/display-driver-uninstaller-download.html) 

# Recomended sites

[The-Guru-Of-3D](https://www.guru3d.com/) 


___
___

# Personal issues

### Overwatch 2 crashing, cause of rising GPU clock

**SPECS:**

- GPU: `RTX 2070 Super`
- CPU: `AMD Ryzen 7 3800X`
- Motherboard: ``ROG STRIX B550-F GAMING (WI-FI)`

**ISSUE:**
It was when playin Overwatch 2. When the game repeatedly crashed when i died, or other apparently "graphical" instances would occur. It crashed, "Closed the game" my screen's froze and any video playing stopped.

**Solution:**
Underclocking my GPU whenever i was playing Overwatch 2. I did this using [MSI Afterburner](https://www.msi.com/Landing/afterburner/graphics-cards) 
These settings worked for me:

![[MSI-Afterburner-Overwatch2-Underclocking-Fix.webp]]

Downgrading GPU driver might yield good results


**Believed Cause:**
I have 2 hypotheses:

1. The game had some issues related to the driver that caused the game to overclock the gpu above the boost clock under certain events. The game needed more gpu, so the driver said higher clock, causing the gpu to panic.

2. Simular to number 1. the driver caused the gpu clock speed to rise above normal, when encountering wierd situations in the game. Overheating the GPU, triggering its safety switches.

SUMMED UP:
> Game bad. GPU driver + game = wierd crashing: Boosted GPU clock overheats GPU

### Disco lights, caused by thermal paste on GPU

**SPECS:**

- GPU: `RTX 2070 Super`
- CPU: `AMD Ryzen 7 3800X`
- Motherboard: ``ROG STRIX B550-F GAMING (WI-FI)`

**ISSUE:**

Having flickering disco light "**Disco of death**" when playing RUST and Flight-Simulator-2020

![[DiscoLights-GPU-ThermalPaste-example01.webp]]
Source: [reddit](https://www.reddit.com/r/XboxSeriesX/comments/t25yqa/anyone_else_experienced_the_nightmare_disco/) 
Another example: [reddit](https://www.reddit.com/r/pcmasterrace/comments/onj80h/after_downloading_nvidia_new_driver_and_turning/) 

These flickerings would occur moments before the game crashed.

**Solution:**

Temperary solutions might be downgrading / updating the GPU driver. Or Undercloking the GPU.

My solution that fixed the problem was to open and clean the GPU. ESPECIALLY Clening and **applying new thermal paste**.

Opening the GPU

![[GPU-Open-01.webp]]

Cleaning and applying new Thermal paste

![[GPU-Circuit-01.webp]]
Its removed in this picture, but it was way to much thermal paste all over the blue main circuit. "It was bad"


**Believed Cause:**

Overheating the GPU under load caused it to crash. 
This is due to degraded thermal paste and / or thermal paste spilling over to places it should not be. ( Conducting electricity were it should not. Then displaying these **Disco of death** lights )