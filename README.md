# Bridged Loop Models

A 3D modeling framework for plant phenotyping written in python.

## Main Features

- Measure plant morphological traits from photogrammetry-derived 3D surface meshes
- Create a new mesh from an existing mesh where every vertex belongs to an edge loop.
- Define plant structure by the bridges, or connections, between loops
- Compare plants by separating position-based information (bent leaves) from

## Additional Features

- Clean up photogrammetry-derived datasets using rule-based approaches to remove unlikely data and add plausible data
- Create procedural models of simulated plants
- Use sunlight simulation models to estimate PAR absorbance and make selections
for ideal plant morphology traits

## Detailed Features

## Mesh to Bridged Loop Model

Convert an existing triangle mesh to a bridged loop model.

1. Slice mesh along multiple directions to extract loop candidates
2. Assess loop candidates and filter out poor-fitting loop candidates
3. Bridge loops by angle and distance

Regenerate mesh from bridged loop model

1. Create triangle mesh from bridged loop model
2. Compare output mesh to input mesh

## Plant Trait Extraction from Bridged Loop Model

Extract phenotypic traits from bridged loop model

1. Define segmentation parameters for a specific crop of interest
2. Segment the bridged loop model into plant(s) and plant organs
3. Calculate and summarize traits for all model segments

# Getting Started

## Installation With Conda:

### First-time installation
Clone the repository:
```commandline
git clone https://github.com/wmpeebles/BridgedLoopModels.git
```

Create a conda environment
```commandline
cd BridgedLoopModels/
conda env create -f environment.yml
```

Activate the environment
```commandline
conda activate BridgedLoopModels
```

Install BLooM
```commandline
pip install -e .
```

Run the tests
```commandline
cd tests/
pytest
```

### Updating to the latest version

Update the environment
```commandline
conda env update -f environment.yml
```

Update loopmodels
```commandline
pip install -e .
```

### Uninstall

Remove the conda environment
```commandline
conda env remove -n BridgedLoopModels
```
