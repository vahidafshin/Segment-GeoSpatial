# Segment-GeoSpatial

This repository showcases the power and versatility of the `segment-geospatial` module for geospatial data analysis and processing. It is inspired by the `segment-anything-eo` repository authored by Aliaksandr Hancharenka. To facilitate the use of the Segment Anything Model (SAM) for geospatial data, the `segment-anything-py` and `segment-geospatial` Python packages were developed and are now available on PyPI and conda-forge. The primary objective is to simplify the process of leveraging SAM for geospatial data analysis with minimal coding effort.

## About the `segment-geospatial` Module

The `segment-geospatial` module is a Python package designed to streamline the process of identifying and masking objects in geospatial data. By integrating SAM capabilities, it allows users to work seamlessly with aerial, satellite, and other forms of geospatial imagery.

Key features include:
- Automatic object masking.
- High-quality segmentation.
- Integration with bounding boxes, text prompts, and other input formats.

## Installation

### Install from PyPI

`segment-geospatial` is available on PyPI. To install, run the following command:

```bash
pip install segment-geospatial
```

### Install from Conda-Forge

`segment-geospatial` can also be installed from conda-forge. It is recommended to create a fresh conda environment for installation. Use the following commands:

```bash
conda create -n geo python
conda activate geo
conda install -c conda-forge mamba
mamba install -c conda-forge segment-geospatial
```

For systems with a GPU:

```bash
mamba install -c conda-forge segment-geospatial "pytorch=*=cuda*"
```

Optional dependencies:

```bash
mamba install -c conda-forge groundingdino-py segment-anything-fast
```

### Install from GitHub

To install the development version from GitHub, run:

```bash
pip install git+https://github.com/opengeos/segment-geospatial
```

### Use Docker

To run `segment-geospatial` using Docker:

```bash
docker run -it -p 8888:8888 giswqs/segment-geospatial:latest
```

To enable GPU support:

```bash
docker run --rm -it --gpus=all nvcr.io/nvidia/k8s/cuda-sample:nbody nbody -gpu -benchmark
```

Start a Jupyter Notebook server:

```bash
docker run -it -p 8888:8888 --gpus=all giswqs/segment-geospatial:latest
```

## Examples

This repository includes several examples demonstrating the capabilities of the `segment-geospatial` module. Each example is accompanied by a detailed explanation and a demo to showcase its functionality.

### 1. Automatic Mask Generator

**File:** `automatic_mask_generator.ipynb`

Description: Demonstrates how to automatically generate object masks from an image using SAM.

Demo:
<img src="Demo/Automatic mask generation.gif">


### 2. High-Quality Mask Generator

**File:** `automatic_mask_generator_hq.ipynb`

Description: Shows how to create high-quality object masks using the High-Quality SAM model.

Demo:

<img src="Demo/Automatic mask generator hq.gif">

### 3. Box Prompts

**File:** `box_prompts.ipynb`

Description: Illustrates the use of bounding box prompts for generating object masks.

Demo:

<img src="Demo/Box prompts.gif">

### 4. Fast SAM

**File:** `fast_sam.ipynb`

Description: Explains how to use the FastSAM model for rapid mask generation.

Demo:

<img src="Demo/Fast sam.png">

### 5. Input Prompts

**File:** `input_prompts.ipynb`

Description: Shows how to use point prompts to generate masks for specific objects.

Demo:

<img src="Demo/Input prompts.gif">



### 6. Swimming Pools Detection

**File:** `swimming_pools.ipynb`

Description: Provides an example of detecting and masking swimming pools using text prompts.

Demo:

<img src="Demo/Swimming pools.gif">

### 7. Text Prompts

**File:** `text_prompts.ipynb`

Description: Explains how to use text prompts to generate masks for specific objects.

Demo:

<img src="Demo/Text prompts.gif">

### 8. Tree Mapping

**File:** `tree_mapping.ipynb`

Description: Demonstrates the identification and masking of trees in aerial imagery using SAMGeo.

Demo:

<img src="Demo/Tree mapping.gif">

## Contributions

Contributions are welcome! Please feel free to fork the repository and submit a pull request with your enhancements.



