+++
title = 'Generate Your Own Music'
platforms = ["windows", "linux"]
requirements = ["pixi", "cuda-non-blackwell"]
source = 'https://github.com/DolicaAkelloEgwel/Generate_Your_Own_Music'
parent = 'https://github.com/masanbasa3k/Generate_Your_Own_Music'
+++

## Link

{{<source-link>}}

## Platforms

{{<platforms>}}

## Requirements

{{<requirements>}}

## Installation

{{<installation>}}

## Usage

### Training a Model

The first step is to train a model. To do this run the following command:

```
pixi train -i PATH_TO_DATASET_FOLDER -o PATH_TO_OUTPUT_FOLDER
```

The dataset path should contain the collection of MIDI files that you wish to use for training. The model files and metadata will then go into the specified output path.

You may also use the following optional command line arguments to control aspects of the training:

```
  -e EPOCHS, --epochs EPOCHS
                        number of epochs for training
  -bs BATCH_SIZE, --batch-size BATCH_SIZE
                        the batch size for training
  -sl SEQUENCE_LENGTH, --sequence-length SEQUENCE_LENGTH
                        the sequence length for training
  -si SAMPLE_INTERVAL, --sample-interval SAMPLE_INTERVAL
                        the sample interval for training
```

### Generating Music

Once a model has been trained, it can be used to generate one or more MIDI files. This is done with the following command:

```
pixi run generate -m PATH_TO_MODEL_FILES -o OUTPUT_FILE_PATH -n NUMBER_OF_OUTPUT FILES
```

This will then create the specified number of MIDI files in the given path. If no number of output files is given, the code will default to generating a single file.

The optional latent dimension argument can also be used:

```
-ld LATENT_DIMENSION, --latent-dimension LATENT_DIMENSION
```

### Playing Music

There is also the option of playing the files with the program. This can be used to play a single file or a folder of MIDI files.

#### Single File

```
pixi run play -f PATH_TO_SINGLE_MIDI_FILE
```

#### Folder of MIDI Files

```
pixi run play -d PATH_TO_FOLDER_OF_MIDI_FILES
```

## Parent Project

{{<parent-link>}}

## Further Info
