Camera-intrinsics-database
==========================

Camera intrinsics database is a place to find the proper calibration (also known as intrinsic matrix) for your camera.
This information is widely used in 3D reconstruction algorithms like SLAM and especially in Augmented Reality.

The goal of this project - to collect and share database of already calibrated cameras for all modern mobile devices in one place.

Contribution
==========================

You can help this project by taking a sequence of photos (Ten photos is usually enough) of one of the calibration patterns with your mobile device.
The pattern images can be found under Patterns directory. Just print it on A4 paper and take a series of photos from different angles. Feel free to 
send them in zip-arhive to ekhvedchenya@gmail.com. Your participation will be noted in contributors list. Also you can ask me for a write-access to repository.
Calibration pattern can be found under Patterns directory of this repo.


To Do
==========================
* Write a command-shell script to walk across all photo sets and pass them through calibration pipeline (OpenCV backend)
and save calibrated database to the YAML files.
* Write a command-shell script to generate a intrinsic database in code (C++, ObjectiveC, Java, C#)

Directory structure
==========================
Patterns directory holds the images of calibration patterns taken by the specific device.
The folder name indicates device using following notation <device-name>[-<camera-position>].
For example, for iPhone 3Gs that has only rear camera the directory name will be "iphone3gs",
For front camera of the iPad2 it would be "ipad2-front", for MBA built-in camera - "mba-mid2011-isight".

Under this directory you can find either images for grid calibration pattern or for circles pattern.
They identified by file prefixes: "grid" and "circles" accordingly.

The file name template: [grid|circles]_XX.[png|jpg|bmp], where XX - is the two-digit counter.
