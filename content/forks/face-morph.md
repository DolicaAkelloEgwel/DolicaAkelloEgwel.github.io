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
source = 'https://github.com/DolicaAkelloEgwel/Face-Morphing'
+++

Generates a face-morphing video by a folder of face images.

![](/images/face-morph.gif)

## Link

{{<source-link>}}

## Platforms

{{<platforms>}}

## Requirements

{{<requirements>}}

## Installation

{{<installation>}}

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