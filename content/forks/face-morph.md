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

## Platforms

{{<platforms>}}

## Requirements

- uv
- ffmpeg

## Installation

1. Install the required software above. The steps to do this will depend on what platform you're using.
2. Clone the [repository](https://github.com/DolicaAkelloEgwel/Face-Morphing).
3. Open the project folder in your terminal or command line, and then enter the following command:

```
uv sync
```

This will have installed all of the required Python libraries. You should now be able to run the face-morphing code.

## Usage

1. Collect some face images. You will need at least two, and they will have to all be 1024x1024.
2. Move these images to the `images` folder in the project directory.
3. Run the following command:
```
uv run code/__init__.py --images images --output output.mp4
```

You should now see a face-morph video called output.mp4 in your project directory. Feel free to run this again with other images, but be sure to either change the name of the output file or backup the output files created from previous runs.