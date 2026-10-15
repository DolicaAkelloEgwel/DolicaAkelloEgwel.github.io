+++
title = 'Face Morph'
platforms = [
    "windows",
    "macos",
    "linux",
    "raspberry-pi"
]
+++

This code allows you to take a folder of images and use them to generate a face-morphing video.

![](/images/face-morph.gif)

## Link

https://github.com/DolicaAkelloEgwel/Face-Morphing

## Platforms

{{<platforms>}}

## Requirements

- pixi

## Installation

1. Install the required software above. The steps to do this will depend on what platform you're using.
2. Clone the [repository](https://github.com/DolicaAkelloEgwel/Face-Morphing).
3. Open the project folder in your terminal or command line, and then enter the following command:

```
pixi install
```

This will have installed all of the dependencies and required Python libraries. You should now be able to run the face-morphing code.

## Usage

You have the opition of aligning videos before running the face-morphing code. You may want to go through this step if your images anre not 1024x1024 and you don't wish to resize them individually.

### Aligning Faces

1. Collect some face images. You will need at least two if you wish to create a video.
2. Run the following command:
```
pixi run python code/utils/align_images.py nonaligned/images/path aligned/images/path --output_size=1024
```  

### Generating a Video

1. Choose images for your video generation. You may have decided to align them beforehand, but make sure that they are 1024x1024.
2. Run the following command.
```
pixi run python code/__init__.py --images input/images/path --output output.mp4
```

You should now see a face-morph video called output.mp4 in your project directory. Feel free to run this again with other images, but be sure to either change the name of the output file or backup the output files created from previous runs.