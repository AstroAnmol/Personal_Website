---
layout: page
title: Avalanching on airless metallic bodies with remnant magnetic field
description: Doctoral Thesis
img: assets/img/project_preview/mag-avalanching.png
importance: 1
category: ["planetary science"] 
---

NASA's OSIRIS-REx mission collected Asteroid Bennu's regolith using the TAGSAM - Touch-and-Go Sample Acquisition Mechanism.
The arm was supposed to touch and collect samples, but unexpectedly, it kept penetrating into the surface.
The spacecraft fired thrusters in order to disengage with the asteroid, or it would have crashed on the surface.
This unexpected behavior was caused by the near-zero cohesion between the asteroid regolith.
The whole ordeal pointed to our limited understanding of regolith dynamics in micro-gravity environments.

While we have been studying regolith processes for traditional (stony) asteroids, NASA is endeavouring to explore a new world.
Psyche is a metallic asteroid in the main belt between Mars and Jupiter.
It is likely a planetesimal - a building block of planets left over from the early solar system.
Researchers think that it is a striped core, just like one inside our Earth.
Therefore, we expect Psyche to have a remnant magnetic field.
Magnetic field could lead to a new cohesion between regolith particles - **Magnetic cohesion**.
I am working to model this magnetic force and understand its effects on bulk regolith properties.

While working through the literature on existing magnetic force models, I realized that most magnetic cohesion studies considered less accurate models based on either Fixed Dipole or Mutual Dipole.
\cite{keaveny2008} developed a more accurate model, “*Inclusion model*,” that includes multipoles along with dipoles.
First, I used this model to develop a new empirical formula to calculate the force between two paramagnetic particles placed in a uniform magnetic field.
We can use this empirical formula to define a more accurate *magnetic bond number*: $B_{mag}=\frac{F_{mag}}{F_{grav}}$.
The bond number helps us compare different forces against surface gravity to understand which force could overpower gravity; making it a significant to research and study.
This work resulted in my first journal publication in the *Planetary Science Journal*.

Since then, I have implemented and validated the “*Inclusion Model*” in an open-source Discrete Element Model (DEM) software: LIGGGHTS.
Currently, I am working on validating the model against  experimental work.
Results to follow soon. Meanwhile here are pretty videos :D

## References

{% bibliography --cited %}