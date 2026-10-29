+++
title = 'Face Morph'
platforms = [
    "windows",
    "macos",
    "linux",
    "raspberry-pi"
]
requirements = [
    "pixi"
]
+++

Generates a face-morphing video by a folder of face images.

![](/images/face-morph.gif)

## Link

https://github.com/DolicaAkelloEgwel/Face-Morphing

## Platforms

{{<platforms>}}

## Requirements

{{<requirements>}}

## Installation

1. Install the required software above. The steps to do this will depend on what platform you're using.
2. Download or clone the [repository](https://github.com/DolicaAkelloEgwel/Face-Morphing).
3. Open the project folder in your terminal or command line, and then enter the following command:

```
pixi install
```

This will have installed all of the dependencies and required Python libraries. You should now be able to run the face-morphing code.

## Usage

### Demo

The files come with a collection of pre-aligned images that can be used for demoing the code. You can run the code on these demo images with the following command:

```
pixi run demo
```

This will create a video in the same directory called output.mp4.

### (Optional) Aligning Faces

Aligning faces helps ensure that each face is positioned in roughly the same part of each image. It is optional, but aligning helps make sure that the resulting video has smoother transitions. 

1. Collect some face images. You will need at least two if you wish to create a video.
2. Run the following command:
```
pixi run align YOUR_NONALIGNED_IMAGES_PATH YOUR_ALIGNED_IMAGES_PATH
```

This will create a collection of aligned face images that are all 1024x1024. Now you are ready to create a video with them.

### Generating a Video

1. Choose images for your video generation. You may have decided to align them beforehand, but make sure that they are 1024x1024.
2. Run the following command.
```
pixi run morph YOUR_INPUT_IMAGES_PATH YOUR_OUTPUT_VIDEO_FILENAME.mp4
```

You should now see a face-morph video as the specified filename.