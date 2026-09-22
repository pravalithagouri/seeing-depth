# seeing-depth
Comparing human depth perception with AI depth-estimation models using controlled 3D visual stimuli.

# About the Project

How do we know what is near and what is far away from a two-dimensional image?

The human visual system reconstructs three-dimensional structure using multiple visual cues, including perspective, texture gradients, shading, occlusion, relative size, and binocular disparity.

Modern computer vision models can also estimate depth from images.

But do artificial vision systems respond to these depth cues in the same way that humans do?

Seeing Depth is an exploratory computational vision project investigating how pretrained depth-estimation models respond when individual depth cues are systematically manipulated in controlled 3D scenes.

The project combines ideas from human visual perception, psychophysics, 3D graphics, and computer vision.


# Research Question

> How do artificial depth-estimation models respond to visual depth cues that humans use to perceive three-dimensional structure?

Rather than evaluating models only on natural photographs, this project uses controlled visual stimuli where individual depth cues can be manipulated independently.

This makes it possible to ask not only whether a model predicts depth correctly, but also which visual information it relies on to make that prediction.

# Experimental Approach

The basic pipeline is:

Blender scene

↓  

Controlled manipulation of depth cues

↓  

Rendered visual stimuli

↓  

Pretrained monocular depth-estimation model

↓  

Predicted depth maps

↓  

Quantitative and visual comparison

The physical geometry of the scene can be kept constant while specific visual cues are changed.

This allows model behaviour to be examined under controlled perceptual conditions.

---

# Planned Experiments

## Experiment 001 — Texture Gradient

Investigate how changes in texture density and texture gradients influence predicted depth.

## Experiment 002 — Perspective

Manipulate linear-perspective information while controlling scene geometry.

## Experiment 003 — Shading

Test how lighting and surface shading influence depth predictions.

## Experiment 004 — Occlusion

Examine how models use object boundaries and occlusion relationships.

## Experiment 005 — Cue Conflict

Create scenes in which two depth cues provide conflicting information and examine which cue dominates model predictions.

Future experiments may also explore binocular disparity and stereo depth estimation.

---

## Tools

The project is being developed using:

- Python — analysis and experiment pipeline
- PyTorch — deep-learning models
- OpenCV — image processing
- Blender — controlled 3D stimulus generation
- Blender Python API — automated scene generation
- NumPy / Pandas — quantitative analysis
- Matplotlib — visualization
- Pretrained depth-estimation models — artificial depth predictions
  

## Project Structure

```text
seeing-depth/
│
├── README.md
├── requirements.txt
│
├── blender/
│   ├── scenes/
│   └── scripts/
│
├── stimuli/
│   └── texture_gradient/
│
├── src/
│   ├── depth_model.py
│   └── utils.py
│
├── analysis/
│   └── texture_gradient.ipynb
│
└── results/
    ├── depth_maps/
    └── figures/
```

The structure will evolve as the project develops.

---

## Why Human Vision?

Computer vision systems and biological vision systems face a similar fundamental problem:

**three-dimensional structure must often be inferred from two-dimensional retinal or image information.**

Human vision science has spent decades investigating the cues and computations that support depth perception.

This project explores whether those ideas can also provide useful tools for understanding artificial vision systems.

---

## Current Status

🚧 **Project in development**

Current milestone:

**Experiment 001 — Texture Gradient**

The first stage is building a controlled Blender stimulus generator before evaluating pretrained monocular depth-estimation models.

Results and analysis will be added as experiments are completed.

---

## About Me

I am a vision neuroscientist and clinical optometrist completing a PhD in Sensory Physiology at Otto-von-Guericke University Magdeburg.

My research focuses on how the visual system represents **3D shape and depth from naturalistic images**, using electrophysiology, human psychophysics, eye tracking, and computational analysis.

I am interested in connecting insights from **biological vision with computational vision, 3D perception, XR, and vision-restoration technologies**.

This project is an independent portfolio project and does not contain unpublished or confidential data, code, or experimental materials from my doctoral research.
