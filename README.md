﻿# Haar Cascade Training Data Preprocessing Simplification

A machine perception project using Python/OpenCV to attempt to streamline the processes of gathering training data for Haar Cascade classifiers on skateboards, and actually use said classifiers to attempt to classify given images.
Although this project was initially created to filter/detect skateboards from video files, it was designed with reusability and reapplication of code to new purposes in mind.

## Motivation

This project was originally created as the final project for Machine Perception Spring 2019.

## Screenshots

TODO screenshot/gif of it drawing a rectangle over skateboard

## Features

This project attempts to streamline the often-laborious process of defining regions of interest in sets of unclassified training data, i.e. the process of cropping thousands of unisolated images of the object of interest when a freely-available, labeled training dataset for that object is not available. 
In other words, this project attempts to remove the tedium of cropping thousands of images of skateboards when trying to acquire a training dataset for a Haar Cascade skateboard classifier.
TODO other parts of the project

## Code Example
TODO

//frameripper //etc?

![[example generated images]](docs/example_images.png "example generated images")
Show what the library does as concisely as possible, developers should be able to figure out how your project solves their problem by looking at the code example. Make sure the API you are showing off is obvious, and that your code is short and concise.
TODO

## Installation/Setup

This project requires the following to be installed:

- Python 2.7.15 or higher (not tested in Python 3)
- cv2 3.4.5 or higher

## Tests

Describe and show how to run the tests with code examples.
TODO

## Usage

In order to use this project's Patented Intellicrop™ automated feature-cropping feature, a directory containing videos of the object you want to filter out filmed under controlled conditions but changing camera angles, or controlled camera angles and changing conditions must be created. In our case, each of our videos consisted of the object in question filmed under static lighting conditions through either:
* revolution of the camera around the object at a given height, or
* movement of the object through the environment, or
* movement of the camera towards and away from the object without changing the clockwise position of the camera relative to the object.

Alternatively, a directory containing a set of training images known to contain the object of interest and nothing else can be created.
Once one or both of the above is done, TODO

> cd src
> python FrameRipper.py VIDEOSPATH [--framecount FRAMECOUNT] 

Arguments:
- `videospath` - path to videos to rip and crop frames
- `framecount` *(optional)* - number of frames to rip for each video


## Credits

We would like to thank Ali Parlakci's Bulk Downloader for Reddit, https://aliparlakci.github.io/bulk-downloader-for-reddit/, for enabling us to easily get a large set of negative images by bulk-downloading images from /r/pics.
We would also like to thank the Cascade Trainer GUI, http://amin-ahmadi.com/cascade-trainer-gui/, for allowing us to easily and and quickly train several Haar Cascade classifiers.