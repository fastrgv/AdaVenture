![screenshot](https://github.com/fastrgv/AdaVenture/blob/master/trim_smallMinotaur.gif)


![screenshot](https://github.com/fastrgv/AdaVenture/blob/master/mcraftAV.jpg)

![screenshot](https://github.com/fastrgv/AdaVenture/blob/master/nuAV.jpg)


Click on the large 7z file under releases to download all source & binaries (Windows,Mac & Linux) or try this link:

https://github.com/fastrgv/AdaVenture/releases/download/v2.1.6/av1may20.7z




==============================================================

Video:  New Open Doorways + Mamba:
https://youtu.be/lXkuM0z0JqA

Video:  Walkthru level 1:  Spartan Temple
https://youtu.be/FNE20lw1AZo

Long Video:  Walkthru level 2:  Minoan Labyrinth
https://youtu.be/oVW205APsS0

Short Video:  Charge of the Minotaur:
https://youtu.be/iRj_SnqXbZc

Short Video:  Omar escapes mamba thru moveable bridge:
https://youtu.be/8qbAJ-JvvXs


# AdaVenture GLFW version

## Whats new:

**ver 2.1.6 -- 29apr20**

* Fixed/restored full-screen on all operating systems;


**ver 2.1.5 -- 18apr20**

* Changes in shaders now assure that OpenGL v3.3 is sufficient to run this app.  This is an issue for older graphics drivers.
* Resolved glfw full-screen problem on RedHat-derived linux distros.
* Updated to glfw v3.3.2.

**ver 2.1.4 -- 31mar20**

* Fixed linux soundLoop overruns due to wrong PID.


**ver 2.1.3 -- 27jan20**

* Fixed occasional sound-task related aborts (linux version).
* OSX & Windows sound still uses proven & reliable SFML libs.

**ver 2.1.1 -- 22jan20**

* Ada sound tasks now use unique identifier for robustness;
* Improved certain sound params.
* Trimmed a few excessively large sound files.


**ver 2.1.0 -- 20jan20**

* Quantum improvement in linux portability by avoiding SFML libs.
* Linux sound uses Ada tasking to implement music loops.

## More change-history at end of file



## AdaVenture Game Description
AdaVenture is a kid-friendly retro point & click game, intended to be a minimal extension to 3D of the 2D Atari game named "Adventure", but with various artistic extrapolations.  Now runs on Windows, OSX, and GNU/Linux.  And the new linux binary now runs on many linux distros!

Set in ancient Persia, it begins outside the castle of the young King Xerxes, who inherited a magical golden chalice from his father, Darius the Great.  Coveted by Greek foes King Leonidas of Sparta and King Minos of Crete, the chalice has been stolen.

Your quest is to seek and return the royal chalice to its pedestal within the castle of Xerxes...a stealth mission to preclude open hostilities.  But, there will be obstacles to overcome.  You must find the keys to various realms, defend yourself against dragons and the Minotaur, avoid snakes and pesky bats who steal things only to drop them in random locations, and survive the maze of the green mamba and crazed scarabs.



## AdaVenture Game Features
* When looking closely at a pickable object, a hand will appear indicating that a click will pick up the object.  When holding an object, another click will drop it at the current location.  Only one object at a time may be carried.

* Works on PCs or laptops running Windows, OSX or GNU/Linux.  And if GNAT is installed you can build it yourself!  But first try the delivered binaries.

* Windows, GNU/Linux and OSX binaries provided, as well as full source. 

* Note that both 32 and 64 bit builds for Windows are delivered.

* Laptop friendly controls;  supports Mac Retina displays in high DPI mode.

* The game has four levels.  One fairly easy campaign in Sparta, with a more difficult variant due to thick dark fog.  These are the top two.  Similarly, there is a tricky campaign in Crete, and an even more difficult dark variant.  These are the bottom two, showing Minotaurs.  You select the desired campaign at the beginning of the game.  You can save the current game by using the v-key.  This allows resumption later.  You must replay from the beginning if you die before saving.  Saving the game state is a relatively new feature that only saves one game.  If a saved game exists, a fifth option appears at screen center to resume that game.

* To change the appearance of the avatar, simply download your favorite MineCraft Skin, rename it to "skin.png" and put it into the ./data/ directory.  You should probably backup the current skin before you do this, in case of trouble.  See http://www.minecraftskins.net/.  See also ./data/avatars/ for a small selection.

* For developers, serves as a great example of modern OpenGL programming in Ada or C++ using GLSL 330, shaders, uniforms and Freetype fonts.

* The Ada bindings to OpenGL & GLFW3 in this app are usable as a standalone library for most any modern Ada graphics project.

* The new sound system for linux enables a build with surprising portability across various linux distros.


## mouse/touchpad/keyboard controls

[You might need to disconnect unused gamecontrollers to prevent spinning!]

Look direction is controlled by touch pad or mouse;

The mouse wheel controls camera zoom.  On MacBooks, a 2-finger swipe simulates the mouse wheel; Zoom can also be controlled with keys n, f, z [Nearer,Further,default];  Note that Zoom changes now show immediately, even when stopped, but Lazy Camera change does not show immediately.


Movement is controlled by the WASD keys or the arrow keys:

		(Up)
	(Lt)	(Dn)	(Rt)
---------------------------

*	 (v)-key					=> save game state to resume later
*   (esc)-key 				=> exit;
*   (space)-key			=> pick or drop
*   mouse-click			=> pick or drop
*  (m)-key		 	=> toggle Mouse-view (1st-person) or avatar(3rd-person)
*  (l)-key			=> toggle camera type:  1)Lazy, 2)Tight

In case of unexpected control problems with the game, or if you want to easily inspect some curious feature (like Jupiter in the night sky), temporarily switch to 1st-person mode with the (m)-key.


### joystick
* joystick:  attitude
* center thumb btn:  forward
* trigger btn:  backward
* side thumb btns:  pick or drop items

------------------------------------------------------------
### gamecontroller
* Lpaddle/Lhat:  movement
* Rpaddle :  attitude
* L/R Shoulder btns:  pick or drop items

------------------------------------------------------------
### controller settings
If the need arises, copy the file "default_settings.txt" to "./data/settings.txt".  Then you can manually edit the floats that define the sensitivity for mouse, keyboard, gamepad & joystick, as well as forward speed of the avatar.


------------------------------------------------------------
------------------------------------------------------------


## required for running:

* graphics card with ample memory & driver that supports OpenGL version 3.3 or later;
* Windows, GNU/Linux or OSX;
* optional game controller or joystick.


## Setup & Running Adaventure:

The application's root directory [./avent/] contains files for deployment on 3 platforms:  1)windows (32+64bit), 2)OS-X, 3)linux, in addition to source code.  If you are NOT running windows, you do not need .dll files.  If you are NOT running OS-X, you do NOT need the subdirectory named ./adaventure.app/.


Mac users see "osx-setup.txt".
Windows users see "windows-setup.txt".


Unzip the archive.  On Windows, 7z [www.7-zip.org] works well for this.

Open a commandline terminal, and cd to the install directory.  If your platform is High-Dpi-capable, type the executable-name followed by a "1", before hittting the (enter-key).  But if the game does not play smoothly, you should run in Low-Dpi mode.

Linux users should type "adaventure_gnu" to start the game.  You may also double click its icon in file manager.  This executable was built on Linux Mint, and tested on RedHat (Scientific-Linux) to not only run well, but to rebuild easily.

Similarly Mac users type "adaventure_osx",  or navigate to the installation directory in Finder and click the "adaventure.app" icon named "AdaVenture".  Note that any jerkiness experienced while running at HiDpi can be elliminated by editting the bundle-controls to force LowDpi.

Windows users type either a) binw32\adaventure32.exe or b) binw64\adaventure64.exe

The install_directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data.

Note that adjustable OpenGL settings should favor performance.  OTOH, this game runs fine on an Intel NUC with embedded Intel graphics, so the graphics demands are modest.


--------------------------------------------------------------------------
Open source Ada developers are welcome to help improve or extend this game.

Please send improvements, comments, suggestions or questions to:

fastrgv@gmail.com



## Included Open Source libraries that allow rebuilding:
* SFML, GLFW, FLAC, ogg, vorbis, openal, freetype
* glext.lib for Windows
* the included "bindings" directory contains Ada interfaces:
	* AdaPngLib
	* gl
	* glfwada
	* FreeTypeAda
	* Kazakov strings, tables
	* SFML

## Rebuild Requirements:
* systems:  Windows, OSX or GNU/Linux
* a recent gnat Ada compiler;  eg. AdaCore
* Xcode g++ compiler, if using OSX

Note that the module that defines the Ada interface to SFML-AUDIO, snd4ada_hpp.ads, was created with the command: "g++ -c -fdump-ada-spec -C snd4ada.hpp" which references a minimalistic C++ utility snd4ada.  Thus, if you redefine the interface snd4ada.hpp, you will need to recreate the interface spec snd4ada_hpp.ads by this method.



## Build instructions for AdaVenture:

Four [pre-compiled] binary executables are delivered, two for Windows, one for gnu/linux and one for OSX.  I believe the Windows executables are fairly portable.  They were built on Windows 10.  The Mac binary, adaventure_osx, should run on most any standard Mac with a recent version of OSX.  The linux binary, adaventure_gnu, is intended to run in the presence of the directory "./libs/gnu", which contains some dynamically loaded libraries that can be, but need not be present on a target system:  GLFW, SFML, FLAC, ogg, vorbis, openal, crypto, freetype.

The distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is older than june 2011, it probably will not run, and you will need to recompile.

Build scripts for GNAT2015 or newer are provided;  and due to a recent script change, a Windows or linux build machine need not have a C++ compiler installed.  Only GNAT-GPL from AdaLibre is required (GNAT has its own g++).

-------------------------------------------------------
**msWin32** => wcmp32a.bat, wcmp32b.bat

**msWin64** => wcmp64a.bat, wcmp64b.bat

Note that the above windows build scripts might need to be editted to reference your actual installation directory for 32bit AdaCore 2017 or 64bit AdaCore 2018 compilers.


-------------------------------------------------------
**MacOSX** => ocmpss.sh:

build script for generating a portable executable that will run on most OSX platforms whether or not they have non-standard libraries GLFW or SFML installed.  This is used to build the executable named adaventure_osx.  Macs with a recent but standard configuration of OSX should be able to rebuild using these scripts, assuming you have GNAT GPL installed, as well as g++ from Xcode.

------------------------------------------------------
**GNU/Linux** => lcmpd.sh:

uses mostly dynamic linking, especially for the non-standard libraries GLFW, as well as other more common shared libraries that are delivered in this bundle under ./libs/gnu/.  These are used to build the [gnu/linux] executable, which should run in the presence of ./libs/gnu/, whether or not your system has those shared libraries installed.


If the delivered linux binary does not run...

* Manually install GNAT GPL from libre.adacore.com/download/.
* Rerun the compile script lcmpd.sh.


### Link Problems during linux build:

On a linux build machine, you might have repairable link errors, depending on its configuration.  If you are missing "libz", you can simply copy "libz.so" from /usr/gnat/lib/gps/ into /usr/local/lib/.  If "libGL" cannot be found, this literally means "libGL.so" was absent.  But you might have "libGL.so.1" present.  In this case, simply create a softlink by changing to the libGL directory, then type the line:

sudo ln -s libGL.so.1 libGL.so  (and enter the admin password)

whence the linker should now be able to find what it wants.  But if there is more than one file libGL.so present on your system, make sure you use the best one;  i.e. the one that uses your accelerated-graphic-driver.


---------------------------------------------------------
**GPR note:**
There is an alternative build system included for those who prefer, and know how to use GPR:  under ./buildScriptsGpr/ .  There are 3 high level shell scripts to drive each:  gnugpr.sh, osxgpr.sh, wingpr.bat.  (They must all be moved up 1 directory to work.)




----------------------------------------------------------------------
## For Developers Only:  Portable Avatar Using Shaders

* This approach encapsulates the details of avatar shape, color, and movement within GLSL shaders and a related code object that defines vertices and texture maps.  The object may be an Ada package or C++ class.

* Programmatic inputs include uniforms for time, position, attitude, & type of motion.  The shaders then offload the realtime computational burdens onto the graphics processor.

* Data that defines shape and color, as well as the uniforms and functions that define behavior, reside completely within the object and shaders.  This data can ultimately be as detailed and refined as your imagination permits.  And any refinements made are not obfuscated in some esoteric or proprietary format with a limited audience, but remain fully portable and easily enhanced by most any developer using Free Open Source tools and compilers.

* One approach would be to completely define the avatar within the shaders alone, possibly without using any texture files.  Just look at the creatures in (glslsandbox.com).  This would require advanced GLSL skills.

* But a huge selection of available MineCraft skins lead to the present avatar object design.

* In this example, the texture object is a cube with radius one that is defined as 6 disjoint cubelets.  The 2 upper quarters map to the head and torso.  The lower half is divided into 4 cubelets that are mapped to arms and legs.  The Minecraft images used for the texture also have 6 parts that map to the limbs, head and torso.

* The result is an utterly portable avatar defined by an image and 4 text files:
	* texture object body, avatarobj.adb
	* texture object spec, avatarobj.ads
	* vertex shader, avatarobj.vs
	* fragment shader, avatarobj.fs
	* any MineCraft Skin png file

* Interfacing game code with such an avatar is simple.  Essentially you need only pass the current uniform values prior to drawing.

* Of course one still needs a decent camera positioning and pointing policy within the game code in order to fully appreciate and exhibit the avatar.




## What is special about this project?

The linux-build of AdaVenture is among very few modern OpenGL games where a single pre-built executable can run on multiple Linux distros without 3rd party add-ons!  There is only one proviso:  "aplay" must be present.

For developers, this project can serve as a testbed for learning modern OpenGL and GLSL.

It uses the Ada programming language and modern OpenGL methods, with textures, shaders and uniforms.  Compiles and runs on Windows, GNU/Linux and Mac OSX systems.

Focusing on portability, transparency, and open source freedom, this project relies exclusively on F.O.S.S. tools:  a thin glfw3 binding, a thin OpenGL binding, a PNG reader by Stephen Sanguine and Dimitry Anisimkov, SFML-Audio with a homebrew binding, a FreeTypeAda binding by Felix Krause, plus string & table utilities by Dmitry Kazakov.

The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used for your own OpenGL Ada project.

For the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many ada-specializations yet to be made.  

This game is a work in progress, so please excuse any scaffolding and debugging code has not been removed.

If you make improvements, please send then to <fastrgv@gmail.com>



--------------------------
## Legal Mumbo Jumbo:


AdaVenture itself is covered by the GNU GPL v3 as indicated in the sources:


 Copyright (C) 2020  fastrgv@gmail.com

 This program is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.

 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.

 You may read the full text of the GNU General Public License
 at <http://www.gnu.org/licenses/>.


## Media Files:

### General Note
The particular choices of sound, image, and fragment shader files [x.fs] delivered are not essential to the function of the game and are easily replaced.


### SoundFiles
Many sounds are from freesound.org and are covered by the Creative Commons Attribution noncommercial license documented in the accompanying file ccnc3_license.txt.  see also:  (http://creativecommons.org/licenses/by-nc/3.0/legalcode/)

Two tracks (for the labyrinth) from incompetech.com (also CC-by-3 license) thanks to Kevin MacLeod (Cephalopod,Dama-May).

Some original Atari sounds were also used.

Credit and thanks to the Godfather of Exotica, Korla Pandit, for the excellent renditions of Turkish Dance and Miserlou...a song so old that its origins are vague, yet was known to have been popular in ancient Persia and the middle-east, as well as to all us fans of Dick Dale!


### ImageFiles 
* the GPL2.0/GPL3.0-only section of OpenGameArt.Org.  
* http://www.mayang.com/textures.  See mayang_license.txt.  
* pixabay.com with a CC0 license.
* http://all-free-download.com/free-photos/.


### ShaderFiles 
Several fragment shader files used were downloaded from http://glslsandbox.com/ and put under ./data/.  All frag. shaders from glslsandbox are under the MIT license (see mit_license.txt).  Existing comments or any identifying information was retained.

In order to make these usable, I had to modernize them to glsl version 330 specifications, and adapt them to utilize some programatic uniforms for input.


### SkyBoxes 

* www.custommapmakers.org/skyboxes.php
* www.OpenGameArt.org;  thanks to Pieter Spiney Verhoeven (cloudy)
* Some beautiful hi-res skyboxes used [from OpenGameArt.org] are the work of Heiko Irrgang <hi@93-interactive.com> and licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License.  To view a copy of this license, visit (http://creativecommons.org/licenses/by-sa/3.0/) or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  See also the accompanying file ccsa3_license.txt.


### Bindings & Utilities

Thanks to Kazakov, Anisimkov, Sanguine and Krause.


## Best Download Sites for my games:

https://github.com/fastrgv?tab=repositories

http://www.indiedb.com/members/fastrgv/games

https://fastrgv.itch.io/

## Video Level 1:
https://youtu.be/Pr0IhvHXvFQ

## Tags
kids,retro,adventure,dragon,castle,maze,labyrinth

-------------------------------------------------------------------------
-------------------------------------------------------------------------

## Update History:

**ver 2.0.6 -- 15jan20**

* Updated Ada binding to glfw.


**ver 2.0.5 -- 11jan20**

* Improved code that reads settings file to allow Dos-Format.
* Updated to GLFW v3.3.1 (released 1jan2020).
* Added option @ center-screen to continue a saved game, if one exists.
* Fixed the broken Apple OSX "bundle".


**ver 2.0.4 -- 09jan20**

* Now castle pool contains reflective water;
* Improved controlability of mouse slew @ HiDpi.
* Added ~/data/settings.txt file to allow users to adjust:
	* Forward/Backward Speed
	* Slew Speed using:
		* keyboard
		* mouse
		* gamepad
		* joystick


**ver 2.0.3 -- 07jan20**

* Improved windows build method;
* Now delivering this GLFW version as the mainstream version;


**ver 2.0.2 -- 25dec19**

* Restored proper fireball speed;
* Finalized code for basic joystick/gamepad function.


**ver 2.0.1 -- 24dec19**

* Fixed some coding errors & omissions that might cause trouble in HiDpi mode.


**ver 2.0.0 -- 23dec19**

* Converted Ada code to use GLFW, rather than SDL2;
* Updated libraries, DLLs, Ada binding;
* Limited gamepad functionality;




**ver 1.5.7 -- 19dec19**

* Instead of delivering two distinct executables for each platform, a single commandline parameter of "0" now signals HighDpi is NOT desired.  Thus, no parameter will prefer HighDpi, if available.  Graphical overload is not usually a problem with AdaVenture.
* Improved font code & anti-aliasing thru corrected OpenGL code parameters.


**ver 1.5.6 -- 31nov19**

* Carnivorous beetles are now deadly if you linger too long.
* Added & improved death-scream sounds.
* Now deliver two executables for Mac/OSX, defaulted to Low-Dpi.


**ver 1.5.5 -- 26nov19**

* Repaired a library problem with the GNU/Linux build that limited portability.
* Added skylight and improved lighting in ninth maze.
* Added frame for castle skylight.


