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

## storm-control

**Website:** https://github.com/ZhuangLab/storm-control  
**Source:** https://github.com/ZhuangLab/storm-control  
**License:** MIT  
**Scope/Description:** storm-control was originally designed for acquiring single molecule localization microscopy data in a manual or semi-automated fashion. At a later point the ability to collect MERFISH data was added. The hardware drivers can all be found in the storm_control\sc_hardware directory.  
**Hardware Supported:** Please see [this](https://github.com/ZhuangLab/storm-control/tree/master/storm_control/sc_hardware) web-page.  

## ScopeFoundry

**Website:** http://www.scopefoundry.org/  
**Source:** https://github.com/ScopeFoundry/  
**License:** BSD  
**Scope/Description:** ...  
**Hardware Supported:** ...  


## bluesky / Ophyd

Part of the bluesky project designed at particle accelerators. Ophyd provides a hardware abstraction that is typically on top of distributed controls for accelerators, but can be used more generally.

**Website:** https://blueskyproject.io/ophyd/  
**Source:** https://github.com/bluesky/ophyd  
**License:** BSD  

## Instrumental
**Website:** https://instrumental-lib.readthedocs.io/en/stable/index.html  
**Source:** https://github.com/mabuchilab/Instrumental  
**License:** GPL-3  
**Scope/Description:** Python-based library for controlling lab hardware like cameras, DAQs, oscilloscopes, spectrometers, and more. It has high-level drivers for instruments from NI, Tektronix, Thorlabs, PCO, Photometrics, Burleigh, and others. 

**Hardware Supported:**  

**Cameras**  
* PCO cameras via PCO SDK
* PCO Pixelfly camera
* Princeton Instr. camera via PICAM SDK
* Photometrics cameras
* TSI cameras
* Thorlabs DCx cameras  

**Lasers**  
* Toptica FemtoFiber  

**Motion**  
* Attocube stages
* Thorlabs APT controller
* Thorlabs Flipper Filters
* Thorlabs Kinesis devices
* Thorlabs TDC001 T-Cube DC Servo Motor Controllers
* Newmark rotation stages
**DAQ**  
* NI-DAQmx

see other devices in [drivers](https://github.com/mabuchilab/Instrumental/tree/master/instrumental/drivers)

## Qudi
**Website:** https://ulm-iqo.github.io/qudi-generated-docs/html-docs/  
**Source:** https://github.com/Ulm-IQO/qudi  
**License:** GPL  
**Scope/Description:** Qudi is a suite of tools for operating multi-instrument and multi-computer laboratory experiments. Originally built around a confocal fluorescence microscope experiments, it has grown to be a generally applicaple framework for controlling experiments.

**Hardware Supported:**  

**Cameras**  
* Andor iXon 897 ultra camera
* Thorlabs DCx camera
* Thorlabs compact USB cameras (uc480)

**Lasers**  
* Coherent OBIS
* LaserQuantum 
* Spectra Physics Millennia 

**Motion**  
* Thorlabs APT controller
* Newport CONEX-AGP controller for Agilis stages
* PI stages (incl. Micos)
* Zaber rotation stage

**DAQ**  
* NI-DAQmx pulse generators and counters (via PyDAQmx)
* FPGA counters and pulse generators

see other devices in [hardware](https://github.com/Ulm-IQO/qudi/tree/master/hardware)

## Lantz
**Website:** https://lantz.readthedocs.io/en/0.3/  
**Source:** https://github.com/LabPy/lantz/tree/0.3  
**License:** [BSD](https://github.com/LabPy/lantz/blob/master/LICENSE)  
**Scope/Description:** Lantz is an automation and instrumentation toolkit. On-the-fly GUI for testing purposes.  

**Hardware Supported:**  

**Cameras**  
* Andor, sCMOS and EM-CCD
* PCO Sensicam

**Lasers**  
* Cobolt 06-01 Series
* Coherent Innova 300 Series
* VFL MPB Communications
* RGB Lasersystems MiniLas Evo laser

**Motion**  
* Prior NanoScanZ
* Sutter filter wheel

**DAQ**  
* NI-DAQmx

**Microscope bodies**  
* Olympus IX and BX

other devices listed in [drivers](https://github.com/LabPy/lantz/tree/master/lantz/drivers)


## ACQ4

**Website:** http://acq4.org

**Source:** https://github.com/acq4/acq4

**License:** MIT

**Scope/Description:** Data acquisition platform focused on optical microscopy (cameras, stages, filters, laser scanning), electrophysiology (mostly patch-clamp), and laser photostimulation. Architecture includes device abstraction layer, acquisition engine, and coordinate system modeling.
## yaq

**Website:** https://yaq.fyi/  
**Source:**  [Gitlab project](https://gitlab.com/yaq) [core python implementation](https://gitlab.com/yaq/yaqd-core-python)
**License:** LGPLv3 (for the core) [some more info](https://yaq.fyi/licensing/)
**Scope/Description:** 
yaq provides a daemon based architecture for interacting with hardware (and services).
yaq uses a [msgpack](msgpack.org) based [RPC](https://yeps.yaq.fyi/100) between daemons and clients running in separate processes.
yaq uses a composition based approach to define common [traits](https://yaq.fyi/traits) to enforce API consistency
**Hardware Supported:**  https://yaq.fyi/hardware/ (and actively growing)

## yaq

**Website:** https://yaq.fyi/  
**Source:**  [Gitlab project](https://gitlab.com/yaq) [core python implementation](https://gitlab.com/yaq/yaqd-core-python)
**License:** LGPLv3 (for the core) [some more info](https://yaq.fyi/licensing/)
**Scope/Description:** 
yaq provides a daemon based architecture for interacting with hardware (and services).
yaq uses a [msgpack](msgpack.org) based [RPC](https://yeps.yaq.fyi/100) between daemons and clients running in separate processes.
yaq uses a composition based approach to define common [traits](https://yaq.fyi/traits) to enforce API consistency
**Hardware Supported:**  https://yaq.fyi/hardware/ (and actively growing)
