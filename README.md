# AI_Microscopy_via_DVD
# Requirements
This was tested on Python 3.7. To install the required packages, use the provided requirements.txt file like so:
```bash
pip install -r requirements.txt
```
# Pre-trained model
A pretrained generator model on the DIV2k dataset is provided in the 'models' directory. It uses 6 inverted residual blocks, with 32 filters in every layer of the generator.

Upsampling is done via phase shifts in the low resolution space for speed.

To try out the provided pretrained model on your own images, run the following:
```bash
python infer.py --image_dir 'path/to/your/image/directory' --output_dir 'path/to/save/super/resolution/images'
```
# DVD Laser Scanner Microscope
The laser scanning microscope is a special light microscope which uses a focused laser beam to scans the sample. The scanning of the laser across the sample is done by driving the laser in x and y direction.  The image is composed in the software by combining the measured light points.

The DVD Laser Scanner Microscope is build from two DVD pick-up heads. The laser of the DVD head is used to illuminate the sample at a tiny spot, focused with the DVD heads own focusing mechanism. The deviation of the laser is done by the pick-up heads lens moving coils.

![image](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/DVDLaserScanner.png)

## Confocal Fluorescence Microscopy
A special case is the confocal laser scanning microscopy that enables the reconstruction of three-dimensional structures from sets of images obtained at different depths. Confocal laser scanning microscopes are often used in combination with fluorescence to study properties of biological samples such as cells.

![Diagram of confocal principle](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/CofocalMicroscope-1024x512.png)

## Image Resolution
The resolution of the image is defined by the number of measurements taken in x direction and the number of lines in y. The maximum resolution is limited by the numerical aperture of the system’s objective lens and the wavelength of the laser as in conventional optical microscopes. In fluorescence observations, the resolution is often limited by the strength of the signal. More sensitive photo-detectors or increasing the intensity of the illuminating laser can compensate.


![Beta-Tubulin in Tetrahymena cell, visualised using GFP-marked antibodies under a commercial confocal microscope. (Pawel Jasnos)](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/Tetrachimena_Beta_Tubulin-300x270.png)


![CD/DVD Pick-Up Head](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/695290805_277-300x225.jpg)

The resolution of a CD/DVD reader must be high enough to read the information on the disk.



![AFM image of pits on a CD Rom. Source: Andreas Kleiner](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/cd_10um-300x263.jpg)



![Technical data CD DVD HDDVD BD. Source: Cmglee](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/Pits-1024x529.png)

 

Prototype Setup
The first prototype set-up uses two pick-up head. One is emitting the laser and scanning in x direction. The second pick-up head carries the sample and moves in y direction. The photo-detector on the laser unit is removed and the signal is captured with a simple photo-diode. The coils are controlled by an Arduino with drive electronics and the images is rendered in Processing.


![Laser image as projected on photo sensor. Visual image makes it more easy to observe and focus.](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/Screenshot-from-2016-12-06-230909-300x170.png)

![DIY Laser Scann of Yeast Cells](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/LaserScann-1024x571.png)


## Second Prototype of a DVD Laser Scanner

![alt](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/DVDLaserPCB-871x1024.png)

Made a PCB to control the coils and the laser current with an Arduino Micro, and some connectors for the laser pick-ups.

![a](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/DVDLaserScanner1-300x168.jpg)

![a](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/DVDLaserScanner2-300x168.jpg)

![s](http://www.gaudi.ch/GaudiLabs/wp-content/uploads/CD2-300x228.png)

CD ROM
