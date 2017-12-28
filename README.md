# Object-Tracker
Object Tracker(based on color and live 4-point selection), using mean-shift and cam-shift

The motivation behind this project was object tracking for a UAV team I'm a part of -> [Aerial Vehicle by Team IFOR](http://www.aerialroboticscompetition.org/2015SymposiumPapers/BirlaInstituteOfTechnology.pdf)

The objective of this project is to run a simple object tracking code based on color scheming of the object selected. It asks the user, based on either the video provided as input or the from the live webcam feed, to select a frame(4 points), which it then proceeds to track.

There is a normalizing function that runs in the back to constantly keep the color at a certain detectable frame. this has been hardcoded to (0,255,0), so a plus would be selecting a frame that has the same RGB values as the normalizer.

Credit to the dev team of Open-CV whose tools I've used for this project.

### Requirements
* Open-CV 2.x
* Numpy

(NOTE - Support for Open-CV 2.x might have stopped, so the code might have been deprecated and needs to be updated to Open-CV 3.x methods)

### Code

* To run - `$python track.py`(for live capture) OR `$python track.py --video 'videopath'`(for tracking off an exisiting video)
* Once the frame opens up, press the `i` button to enter the input mode, here is where you select 4 points via the left mouse button
* Once selected, press `enter`
* The frame will track now track the movement of that selected frame
* Press `q` to quit.
