+++
title = 'Gender Detection'
platforms = ["windows"]
source = 'https://github.com/DolicaAkelloEgwel/gender-detection-keras'
parent = 'https://github.com/arunponnusamy/gender-detection-keras'
requirements = [
    "pixi"
]
+++

Detects the gender of the faces present in a single image or webcam input.

![](/images/gender-detection-output.jpg)

## Link

{{<source-link>}}

## Platforms

{{<platforms>}}

## Requirements

{{<requirements>}}

## Installation

{{<installation>}}

## Usage

By default, the code uses a gender-detection model that was trained by Arun Ponnusmay. This will have to be downloaded if you are running the code for the first time.

### Single Image

To detect the gender of the faces in a single image, run the following command:
```
pixi run detect-gender --image YOUR_IMAGE_PATH
```

### Webcam

To continuously detect the gender of faces in the webcam input, run the following command:
```
pixi run detect-gender --webcam
```

### Training a Custom Model

### Using a Custom Model

To use a custom model, the gender-detection can be run with the following commands:

#### Single Image

```
pixi run detect-gender --image YOUR_IMAGE_PATH --model YOUR_MODEL_PATH
```

#### Webcam

```
pixi run detect-gender --webcam --model YOUR_MODEL_PATH
```

## Parent Project

{{<parent-link>}}

## Further Info
