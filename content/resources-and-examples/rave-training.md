+++
title = 'Rave Training'
platforms = [
    "linux",
]
+++

RAVE is a tool that allows for real-time audio generation. This is guidance on how to setup a Python environment that is suitable for training a RAVE model.

A Linux machine is required for training. However, once your training is complete, it should be possible to export a model that may be used to generate audio in MacOS, Raspberry Pi, Windows and Linux. The model will have to be loaded in Max/MSP or Pure Data with the [nn~](https://github.com/acids-ircam/nn_tilde) extension or SuperCollider with the [nn.ar](https://github.com/elgiano/nn.ar) extension.

> [!primary] RAVE on a Raspberry Pi
> Be aware that you must export your model with a particular argument if you wish to use it on a Raspberry Pi.

## Platforms

{{<platforms>}}

## Requirements

- A CUDA-compatible GPU. This cannot be a GPU that uses the newer Blackwell architecture.
- A collection of audio files that are alltogether at least an hour long. Go [here](https://forum.ircam.fr/article/detail/training-rave-models-on-custom-data/) to see IRCAM's guidance on data preparation.
- libsox-dev

## Installation

## Usage

## Further Reading