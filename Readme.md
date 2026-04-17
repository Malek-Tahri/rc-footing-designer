# RC Footing Designer

Isolated footing design according to **ACI 318-19**.

## Background

This repository is a rewrite of a prototype I originally built in **2021**.  
The first version lived entirely inside a single exploratory Jupyter notebook. It worked for testing ideas, but calculations, plotting, and experiments were all mixed together, which made the code difficult to validate, extend, or reuse.

This version rebuilds the project with a clearer structure and more explicit numerical implementations of the footing design procedures. The main focus is the **core calculation logic**, starting with soil pressure distribution and extending to more complex cases involving biaxial bending.

## Current Work

The current notebook implements:

- Elastic soil pressure distribution for rectangular footings  
- Corner pressure calculation under axial load and biaxial moments  
- Visualization of the pressure field  
- Detection of uplift when eccentricity exceeds the kern limits

Elastic cases have been checked against **Autodesk Robot Structural Analysis** results.

## In Progress

Implementation of an **iterative neutral axis solver for large eccentricity cases**  
(biaxial bending beyond the kern where part of the footing loses contact with the soil).

## Repository Structure

```
rc-footing-designer/
├── .gitignore
├── README.md
├── pyproject.toml
├── scope.md
├── docs/
│   └── .gitkeep
├── examples/
│   └── .gitkeep
├── notebooks/
│   ├── input.py
│   └── neutral_axis_finder.ipynb
├── src/
│   └── .gitkeep
└── tests/
    └── .gitkeep
```
