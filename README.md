# Major bug found downloading error since 5.5.1 selection binary - Use original manual
# WON'T WORK WINDOWS 11 5.3 TO 5.4 PROTECT ERROR 

# LightmassConfiguration
LightmassConfiguration is a script made for Unreal Engine 5 to allow to change from Unreal's CPU Lightmass to GPU Lightmass (made by Luoshuang for the Unreal Forums) and back. Since there are no options in GPU Lightmass, the script also allows anyone to change bake quality levels without the need to even restart Unreal Editor. 

This version comes from the original work at  [LightmassConfiguration Unreal 4.*](https://github.com/sgeraldes/LightmassConfiguration)

If you'd like to support the original author, you can donate by going to the code at 

 [LightmassConfiguration Unreal 4.*](https://github.com/sgeraldes/LightmassConfiguration)

clicking "Sponsor" on the top or directly on sgeraldes patreon page here: https://www.patreon.com/LightmassConfigurator

You can donate from $1 to $15 and any donation will be used to keep support the authors work.

# Prerequsites

[Download the Epic Games Launcher From the Epic Games Store](https://store.epicgames.com/en-US/download)

You must first have the latest version installed having restarted your PC earlier and get the latest updates using the "Settings" tab.




# Usage
To use:

Unreal 5.3

**Win RAR decompressor**

Simply download [LightmassConfigurationUE5](https://github.com/jimshalo10/LightmassConfigurationUE5/archive/refs/heads/master.zip)

Right click select WinRAR "Extract to LightmassConfigurationUE5-master"

**Windows Explorer decompressor (more complex)**

Download [LightmassConfigurationUE5](https://github.com/jimshalo10/LightmassConfigurationUE5/archive/refs/heads/master.zip)
If you use Windows Explorer decompress. Right click on the file in Downloads directory "LightmassConfigurationUE5-master.zip" Select "Properties"

After decompression

In the new box at the bottom tick the box marked "Unblock", the click "Apply" then click "Ok"

 
- On LightmassConfigurator.bat, Right Click and select "Run as Administrator" it will ask for admin permissions and do the rest, including downloading GPU Lightmass to the proper folder, prompting you each step of the way.

- If you have a Windows Defender error, or permission error it means you have not selected "Unblock" delete the file "LightmassConfigurationUE5-master.zip" and start again, following the Window Explorer decompression to unblock the zip file.
  


original Unreal 4-

Simply download [LightmassConfiguration.zip](https://github.com/sgeraldes/LightmassConfiguration/archive/master.zip) and decompress to any folder (empty is better)

# Background and use case
I made a script that will perform a batch of checks and allow to change from GPU bake quality without the need to restart Unreal. It will also check quite a few other things. Hope it helps someone.

It currently works with Unreal Engine 5.3.2, but can easily adapted for ther versions if needed.

# Requirements
- Windows 10 (not tested in other versions) Windows 11, Windows 7 and Windows 8 are not currently supported 
- Admin privileges

- The latest Nvidia drivers versions R525 U3 (528.02)

# Features
The script has the following features:

    Show you the version of Nvidia drivers running (and any other display driver that's running, i.e.: Intel HD)
    
    Check if you have TDR settings as recommended, IF NOT: the script will ask you to do the changes for you (optional)
    
    Allows changing GPU Lightmass quality settings (fast preview, medium, high-ultra, extreme) without needing to restart unreal.
    Backup CPU lightmass for you and give you the option to go restore it later
    
    It will override BaseLightmass.ini on your Unreal folder (it will first backup in the zip archive the version you have and allow to restore at will).
    
    Checks if GPU Lightmass is installed, if not...
        Download the latest version of GPU Lightmass for you from Luoshuang's links
        Download 7Z.exe to quickly backup and perform decompression of the files in the archives
        Finds the installation directory of Unreal, and unzip the files there according to the quality you select (will prompt you for it)
        
    If UnrealEd is running, the script will disable the option to change GPU and CPU lightmass as it needs to access files that are in use to do so.

Please note: The script will give an error while copying when trying to change the quality settings with Unreal Ed running. That's perfectly fine, the file is just been copied over to be sure it remains the same. 


Also note: the script can't change from CPU to GPU lightmass while the Unreal Editor is running, so the script will check for that and disable the option accordingly.



# Updates

UPDATE 1st November 2023 Announcement for Unreal Engine 5.3 from Epic Games Launcher posted on Unreal Engine Forum on

[Luoshuang’s GPULightmass thread](https://forums.unrealengine.com/t/luoshuangs-gpulightmass/109474/2489)


UPDATE 17th November 2023 updates for 5.3.2 by [jimshalo10 aka Jimbohalo10](https://forums.unrealengine.com/u/Jimbohalo10)



UPDATE 06/03/2020 Updated to 4.24.1

UPDATE 12/11/2018 v0.3.2: Updated to work with Unified settings for UnrealEd 4.21 and 4.21.1. Updated minimum Nvidia GPU Driver Version to 411.31

UPDATE 08/23/2018 v0.2: Modified to allow easier updates of the engine. Fixed some bugs. better detection of some parameters and added a fail-safe in case it fails.TDR settings now in decimal instead of hexa.

UPDATE 08/23/2018 v0.2.1: The script now actually checks for driver version and warns the user if the driver does not meet the requirement. 
