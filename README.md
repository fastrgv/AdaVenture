![screenshot](https://github.com/fastrgv/AdaVenture/blob/master/mcraftAV.jpg)

![screenshot](https://github.com/fastrgv/AdaVenture/blob/master/introAV.jpg)

Click on the large tar.gz file under releases to download all source & binaries (both Mac & Linux), or try this link:

https://github.com/fastrgv/AdaVenture/releases/download/v1.2.6/av29jan18.tar.gz


# AdaVenture

## Whats new:

Video:  Omar escapes mamba thru moveable bridge:
https://youtu.be/8qbAJ-JvvXs


**ver 1.2.6 -- 29jan18**

* Generally upgraded Virtual Camera System;
* Higher perspective in maze rooms;
* Improved camera handling logic with two options toggled with the L-key:
	* new Lazy camera default for better theatrics, or
	* classic tight camera for almost first-person control;
	* as before, first-person mode is still toggled with M-key.
* Darker [as intended] maze9;

**ver 1.2.5 -- 10jan18**

* Found & fixed the numerics:argument-error causing occasional aborts;
* Newest Blinn-Phong light shaders include gamma correction;
* Adjusted sizes of avatar & chalice;


**ver 1.2.4 -- 5jan18**

* Added new "darkmaze" to chapter 2 adventure on the far side of the labyrinth of the Minotaur that now hides the chalice (modeled after the classic "orange" maze #2);
* Added a mapRoom directory to help lost souls;
* Improved shaders to include full Phong light modeling, with ambient, diffuse, and specular attenuated lighting effects.  Added glowing chalice;

**ver 1.2.3 -- 27dec17**

* Updated storyline so chapter 2 is more challenging.
* Repaired mamba;  improved shader coding.
* Replaced hidden maze passages with the classic moveable bridge;


**ver 1.2.2 -- 17dec17**

* Significant improvement in maze FOG realism;
* Nice looking low-hanging FOG added to exterior, including skybox.
* Added music, more sounds.
* Logic corrections.


**ver 1.2.1 -- 4dec17**

* Updated to SDL v2.0.7 on Linux, Windows.
* Updated to SDL v2.0.7x on OSX.
* Restore reading controller settings file using intrinsic Exists() ftn.
* The green mamba is now even more ominous with a head raised to spit in your eyes.  However, you might survive if you are holding a sword.


## More change-history at end of file



## AdaVenture Game Description
AdaVenture is a kid-friendly retro point & click game, essentially intended to be a minimal extension to 3D of the original 2D Atari game named "Adventure".  Now runs on Windows, OSX, and GNU/Linux.

Set in ancient Persia, it begins outside the castle of the young King Xerxes, who inherited a golden chalice from his father, Darius the Great.  Coveted by Greek foes King Leonidas of Sparta and King Minos of Crete, the chalice has been stolen.

Your quest is to seek and return the royal chalice to its pedestal within the castle of Xerxes...a stealth mission to avoid open hostilities.  But, there will be obstacles to overcome.  You must find the keys to various realms, defend yourself against dragons and the Minotaur, avoid snakes and pesky bats who steal things only to drop them in random locations, and survive the maze of the green mamba.



## AdaVenture Game Features
* When looking closely at a pickable object, a hand will appear indicating that a click will pick up the object.  When holding an object, another click will drop it at the current location.  Only one object at a time may be carried.
* Works on PCs or laptops running Windows, OSX or GNU/Linux.  And if GNAT is installed you can build it yourself!  But first try the delivered binaries.
* Windows, GNU/Linux and OSX binaries provided, as well as full source. 
* Laptop friendly controls;  supports Mac Retina displays in high DPI mode.
* Serves as an example of modern OpenGL programming in Ada or C++ using GLSL 330 and shaders.
* The Ada bindings to OpenGL & SDL2 in this app are usable as a standalone library for most any modern Ada graphics project.
* Currenly, the game has two easy campaigns:  Sparta or Crete.  So there is not yet any reset capability...you must replay from the beginning if you die.  You select the desired campaign at the beginning of the game.
* To change the appearance of the avatar, simply download your favorite MineCraft Skin, rename it to "skin.png" and put it into the ./data/ directory.  You should probably backup the current skin before you do this, in case of trouble.  See http://www.minecraftskins.net/.  See also ./data/avatars/ for a small [untested] selection.



## mouse/touchpad/keyboard controls

[You might need to disconnect unused gamecontrollers to prevent spinning!]

Look direction is controlled by touch pad or mouse;

Movement is controlled by the WASD keys or the arrow keys:

		(Up)
	(Lt)	(Dn)	(Rt)
---------------------------

*   (esc)-key 			=> exit;
*   (space)-key			=> pick or drop
*   mouse-click			=> pick or drop
* (m)-key or (F1)-key	=> toggle mouse-view (1st-person) or avatar(3rd-person)
* (l)-key => toggle camera type:  1) Lazy,  2) Tight

In case of [unforseen] problems with the game, temporarily switch to 1st-person mode with the (m)-key.


### joystick
* joystick:  attitude
* thumb btn:  forward
* trigger btn:  backward
* other btns:  pick or drop items

------------------------------------------------------------
### gamecontroller
* Lpaddle/hat:  attitude
* Rpaddle :  movement
* btns:  pick or drop items

------------------------------------------------------------
### controller settings
If the need arises, copy the file "default_settings.txt" to "settings.txt".  Then you can manually edit the integers that define the controller-button-assignments or the floats that define the sensitivities.


------------------------------------------------------------
------------------------------------------------------------


## required for running:

* graphics card with ample memory & driver that supports OpenGL version 3.3 or later;
* Windows, GNU/Linux or OSX;
* optional game controller or joystick.
* OSX:  must have OpenAL.framework, which comes on v10.4 and newer


## Open Source libraries included that allow rebuilding:
* SFML, SDL2, FLAC, ogg, vorbis, openal
* glext.lib for Windows
* the included "bindings" directory contains Ada interfaces:
	* AdaPngLib
	* gl
	* sdlada

## Rebuild Requirements:
* systems:  Windows, OSX or GNU/Linux
* a recent gnat compiler
* Xcode g++ compiler, if using OSX

Note that the module that defines the Ada interface to SFML-AUDIO, snd4ada_hpp.ads, was created with the command: "g++ -c -fdump-ada-spec -C snd4ada.hpp" which references a minimalistic C++ utility snd4ada.  Thus, if you redefine the interface snd4ada.hpp, you will need to recreate the interface spec snd4ada_hpp.ads by this method.


## Setup & Running Adaventure:
Unzip the archive.
Windows users may see some error messages pertaining to directory links.  These can be ignored.
Open a commandline terminal, and cd to the install directory.

Linux users should type "adaventure_gnu" to start the game.  You may also double click its icon in file manager.

Similarly Windows users type "adaventure.exe".  Note the DLLs must be collocated.

Mac users may initiate the game by opening a terminal, navigating to the install_directory and typing "adaventure_osx",  or by navigating to the installation directory in Finder and clicking the "adaventure.app" icon named "AdaVenture".

The install_directory should contain a subdirectory named "data".  It contains shaders, skyboxes, sound and texture data, as well as the puzzle definitions.

--------------------------------------------------------------------------
Open source Ada developers are welcome to help improve or extend this game.

Developer or not, send improvements, comments, suggestions or questions to:
fastrgv@gmail.com




## Build instructions for AdaVenture:

Three [pre-compiled] binary executables are delivered, one for Windows, one for gnu/linux and one for OSX.  I don't know how portable the Windows executable is, but it was built on Windows 10 in 32-bit mode.  The Mac binary, adaventure_osx, should run on most any standard Mac with a recent version of OSX.  The linux binary, adaventure_gnu, is intended to run in the presence of the directory "./libs/gnu", which contains some dynamically loaded libraries that can be, but need not be present on a target system:  SDL2, SFML, FLAC, ogg, vorbis, openal, crypto.

The distributed linux executable requires glibc v2.14 or newer.  That means if your distribution is older than june 2011, it probably will not run, and you will need to recompile.

Build scripts for GNAT2015 or newer are provided.  Suggestions or help improving the build process is welcome. 

Three scripts for each OS have the form Xd.sh, Xs.sh, Xss.sh, where the "d" represents "dynamic", and produces the smallest executable.  The "ss" represents the "most static" choice, using more static libraries making its executable larger.  I believe that all of them should work.

Note that due to a recent script change, a linux build machine need not have a C++ compiler installed.  Only GNAT from AdaCore is required.

-------------------------------------------------------
**msWin32** => wcmp.bat

build script that requires libraries included in ./libs/win/.


-------------------------------------------------------
**MacOSX** => ocmpss.sh:

build scripts for generating a portable executable that will run on most OSX platforms whether or not they have non-standard libraries SDL2 or SFML installed.  This is used to build the executable named adaventure_osx.  Macs with a recent but standard configuration of OSX should be able to rebuild using these scripts, assuming you have GNAT GPL installed, as well as g++ from Xcode.

------------------------------------------------------
**GNU/Linux** => lcmpd.sh:

utilize increasingly static linking, especially for the non-standard libraries SDL2 & SFML, as well as other more common shared libraries that are delivered in this bundle under ./libs/gnu/.  These are used to build the [gnu/linux] executable, which should run in the presence of ./libs/gnu/, whether or not your system has those shared libraries installed.


If the delivered linux binary does not run...

* Manually install GNAT GPL from libre.adacore.com/download/.
* Rerun the compile script lcmpd.sh.

### Link Problems during linux build:

On a linux build machine, you might have repairable link errors, depending on its configuration.  If you are missing "libz", you can simply copy "libz.so" from /usr/gnat/lib/gps/ into /usr/local/lib/.  If "libGL" cannot be found, this literally means "libGL.so" was absent.  But you might have "libGL.so.1" present.  In this case, simply create a softlink by changing to the libGL directory, then type the line:

sudo ln -s libGL.so.1 libGL.so  (and enter the admin password)

whence the linker should now be able to find what it wants.  But if there is more than one file libGL.so present on your system, make sure you use the best one;  i.e. the one that uses your accelerated-graphic-driver.



----------------------------------------------------------------------
## For Developers Only:  Portable Avatar Using Shaders

* This approach encapsulates the details of avatar shape, color, and movement within GLSL shaders and a related code object that defines vertices and texture maps.  The object may be an Ada package or C++ class.

* Programmatic inputs include uniforms for time, position, and attitude.  The shaders then offload the realtime computational burdens onto the graphics processor.

* Data that defines shape and color, as well as the uniforms and functions that define behavior, reside completely within the object and shaders.  This data can ultimately be as detailed and refined as your imagination permits.  And any refinements made are not obfuscated in some esoteric or proprietary format with a limited audience, but remain fully portable and easily enhanced by most any developer using Free Open Source tools and compilers.

* One approach would be to completely define the avatar within the shaders alone, possibly without using any texture files.  Just look at the creatures in (glslsandbox.com).  This would require advanced GLSL skills.

* But a huge selection of available MineCraft skins lead to the present avatar object design.

* In this example, the texture object is a cube with radius one that is defined in 6 disjoint cubelets.  The 2 upper quarters map to the head and torso.  The lower half is divided into 4 cubelets that are mapped to arms and legs.  The Minecraft images used for the texture also have 6 parts that map to the limbs, head and torso.

* The result is an utterly portable avatar defined by an image and 4 text files:
	* texture object body, avatarobj.adb
	* texture object spec, avatarobj.ads
	* vertex shader, avatarobj.vs
	* fragment shader, avatarobj.fs
	* any MineCraft Skin png file

* Interfacing game code with such an avatar is simple.  Essentially you need only pass the current uniform values prior to drawing.

* Of course one still needs a decent camera positioning and pointing policy within the game code in order to fully appreciate and exhibit the avatar.




## what is special about this project?
Uses the Ada programming language and fully modern OpenGL methods, with textures, shaders and uniforms.  Achieves version 3.3 core profile contexts.  Compiles and runs on Windows, GNU/Linux and Mac OSX systems.

Focusing on portability, transparency, and open source freedom, this project relies on a thin SDL2 binding from Dan Vazquez, a thin OpenGL binding from "Lumen", a PNG reader by Stephen Sanguine, and SFML-Audio (because of its elegant audio interface).

The Ada bindings are thin, so the relationship to C++ methodology is transparent.  Developers should note that these Ada bindings can be used for any OpenGL Ada project.

For the C++ programmer the code should be easy to comprehend; and for the experienced Ada programmer there are many potential improvements to be made.  Suggestions are welcomed, as are coding or design improvements.  If you make improvements, please send then to fastrgv@gmail.com



--------------------------
## Legal Mumbo Jumbo:


AdaVenture itself is covered by the GNU GPL v3 as indicated in the sources:


 Copyright (C) 2017  fastrgv@gmail.com

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

One track from incompetech.com (also CC-by-3 license) thanks to Kevin MacLeod.

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
* www.OpenGameArt.org
* Some beautiful hi-res skyboxes used [from OpenGameArt.org] are the work of Heiko Irrgang <hi@93-interactive.com> and licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License.  To view a copy of this license, visit (http://creativecommons.org/licenses/by-sa/3.0/) or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  See also the accompanying file ccsa3_license.txt.



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

## Update History


**ver 1.2.0 -- 11nov17**

* added prebuilt executables for msWindows;
* added working build scripts for msWindows;
* Corrected dragon roar logic on reentry;
* Improved dead dragon visibility;
* Removed unused libraries;


**ver 1.1.2 -- 14jul17**

* Updated linux scripts to use a) rebuilt SFML v2.4.2;  b) AdaCore 2017.
* Introduction now mentions that m-key toggles the Avatar.
* Updated OSX scripts to use SFML v2.4.2;
* Added startup messages giving OGL version/profile.
* Added scary hiss sound warning when snake is near;
* Added locked door to labyrinth requiring black key.



**ver 1.1.1 -- 2mar17-19may17**

* Include statically linked linux exe for enhanced portability.
* Repaired a rendering error that failed to draw items dropped on the labyrinth floor.
* Removed deprecated OpenGL commands and enums that may have caused aborts.
* Added fantasy tree in labyrinth;  Zoroastrian embellishment on castle.
* Improved OpenGL error checking.
* Added an avatars directory loaded with a few alternates.



**ver 1.1.0 -- 5feb17**

* Repaired pick logic, particularly while in 3rd person (avatar) mode.  Now, whenever a hand appears an object is pickable, and the avatar becomes translucent.
* Added illumination effect within castle when golden chalice is restored.


**ver 1.0.9 -- 5jan17**

* Corrected a duplicate window glitch.
* Refined compiler scripts.


**ver 1.0.8 -- 29dec16**

* Revised the avatar programming to allow the use of any Minecraft Skin.  You can simply rename your favorite png file to use it in the game.  See instructions in "game features".
* Added WASD keys for movement.
* Improved build system to be compatible with more linux distros.
* Improved OpenGL coding to run on less capable graphics hardware.

**ver 1.0.7 -- 20dec16**

* Added a Tux-the-penguin avatar.  Use the (F1)-key or (m)-key to toggle between mouse view (first person) and a third person avatar view.  This enhancement required the implementation of a preliminary camera handling strategy, which in general can be quite complex.
* Fixed the handlers for game controllers:  joysticks or gamepads.


**ver 1.0.6 -- 2dec16**

* Improved linux build scripts, with varying degrees of static linking.  See build instructions.
* Now uses an improved interface binding Ada to SFML audio.
* Now using SFML 2.4.1.
* Repaired OSX bundling.
* Revised labyrinth.
* New prolog screen allows user to select game (1 or 2).


**ver 1.0.4 -- 3nov16**

* Enhanced castle.
* Added second level.  The Greeks are at it again!  This time the Minoans steal the coveted chalice.  The "orange" Atari maze leads to the labyrinth of the Minotaur;  the Red Dragon and the Bat are increasingly problematic.
* Added an endgame tribute to Korla Pandit, an extraordinary musician, and one of my favorites.


**ver 1.0.3 -- 10oct16**

* Improved sword & chalice icons.
* Fixed bad dragon behaviors.
* Added water feature with moorish pillars to castle.
* other minor improvements including a brighter world upon success.
* improved drawing methods for moorish arches using distance-sort.


**ver 1.0.2 -- 22sep16**

* Maze has many improvements.  It is now redesigned to match the "blue" maze from the original Atari Adventure game.  This involves weird and puzzling interconnections.
* Added a pesky bat, a lethal red-dragon, and an avoidable green-mamba to maze.  Beware!


**ver 1.0.1 -- 16sep16**

* improved final sound sequence;  added original roar to dragon encounters.
* significant improvements to scene transitions and views through doorways.
* larger, actual size castle within skybox exterior scene.
* improved dragon trajectory.


**ver 1.0.0 -- 9sep16**

* Initial version with only 1 level.  Enhancements and more levels coming.
* Foggy maze; dragon, keys to various realms, bat, golden chalice.



