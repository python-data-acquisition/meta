# Existing python packages for microscope hardware control

**NOTE: This list is a work in progress - if you would like your software added, please submit a PR**

Entries should follow the following template:

## package name

**Website:** The url of the package website (if different from the source repository)  
**Source:** The URL (e.g. on github) of the project source
**License:** The (hopefully open source) license used  
**Scope/Description:** What the package tries to accomplish  

**Hardware Supported:**  
* camera 1
* stage 1
* etc

I'll start with python-microscopy to get the ball rolling

## python-microscopy

**Website:** http://www.python-microscopy.org  
**Source:** https://github.com/python-microscopy/python-microscopy  
**License:** GPLv3 (although some components may be able to be licensed more permisibly on request)  
**Scope/Description:** python-microscopy is a large package including a farily mature microscope control GUI as well as a lot of functionality for analysis and postprocessing of microscopy data, especially for single molecule localization experiments. The hardware drivers are found within the source tree in the PYME\Acquire\Hardware subdirectory.

**Hardware Supported:**  
* Andor IXon
* Andor Zyla (probably also Neo, but not well tested)
* Hamamatsu Orca Flash
* Thorlabs DCC1240 (maybe also DCC3240)
* IDS uEye industrial cameras (definitely UI306x, UI327x, UI324x, probably others)
* Ocean Optics spectrometers (probably suffering from bitrot)
* PI piezos (using e255, e662, e709 and e816 controller interface boards, covers most PI piezos, likely easily modifyable to new controllers)
* PI piezo linear motor stages using the C867 controller (M686 stage and similar)
* PI stepper motor stages using the Mercury command set
* Marzhauser Tango translation stages
* Thorlabs MG17?? piezos (this was a 3-axis stage, somewhat dated now)
* Coherent OBIS lasers
* MPB Lasers
* Cobolt lasers
* Matchbox lasers
* Omicron Phoxx lasers
* AA Optoelectronics AOTF
* Simple voltage controlled AOTF (via Arduino)
* Prior Lumen (arclamp)
* Oriel Cornerstone (arclamp and monochrometer)
* Thorlabs FW102B filter wheels
* Thorlabs PM100USB power meter
* TI LightCrafter DMD
* Custom Arduino based "IO slave" (analog, & digital IO)
* Nikon TE2000 stand
* Nikon Ti stand
* 3D Connexion "Space Navigator" 3D mouse
