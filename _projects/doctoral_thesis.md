---
layout: page
title: Avalanching on airless metallic bodies with remnant magnetic field
description: Doctoral Thesis
img: assets/img/project_preview/mag-avalanching.png
importance: 1
category: ["Planetary Regolith Mechanics"] 
related_publications: true
---

NASA's OSIRIS-REx mission collected Asteroid Bennu's regolith using the TAGSAM - Touch-and-Go Sample Acquisition Mechanism.
The arm was supposed to touch and collect samples, but unexpectedly, it kept penetrating the surface.
The spacecraft fired thrusters to disengage with the asteroid, or it would have crashed on the surface.
The near-zero cohesion between the asteroid regolith caused this unexpected behavior.
The whole ordeal pointed to our limited understanding of regolith dynamics in micro-gravity environments.


<div style="max-width:640px;margin:0 auto;" class="my-3">
    <iframe src="https://youtube.com/embed/LJBv4reH9IU" title="YouTube video player" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen
                    style="width:100%;height:360px;border:0;">
    </iframe>
</div>
<div class="caption">
        OSIRIS-REx's TAGSAM operation. Notice how the arm sinks in when it touches the surface of the asteroid.
</div>


While we have been studying regolith processes for traditional (stony) asteroids, NASA is endeavouring to explore a new world.
Psyche is a metallic asteroid in the main belt between Mars and Jupiter.
It is likely a planetesimal - a building block of planets left over from the early solar system.
Researchers think that it is a striped core, just like one inside our Earth.
Therefore, we expect Psyche to have a remnant magnetic field.
Magnetic field could lead to a new cohesion between regolith particles - **Magnetic cohesion**.
I am working to model this magnetic force and understand its effects on bulk regolith properties.

While working through the literature on existing magnetic force models, I realized that most magnetic cohesion studies considered less accurate models based on either Fixed Dipole or Mutual Dipole.
{% cite keaveny2008 %} developed a more accurate model, **Inclusion model**, that includes multipoles along with dipoles.
First, I used this model to develop a new empirical formula to calculate the force between two paramagnetic particles placed in a uniform magnetic field.
We can use this empirical formula to define a more accurate **magnetic bond number**:
$$B_{mag}=\frac{F_{mag}}{F_{grav}}.$$
The bond number helps us compare different forces against surface gravity to understand which force could overpower gravity; making it a significant to research and study.
This work resulted in my first journal publication in the *Planetary Science Journal*: {% cite sikka_development_2023 %}.

Since then, I have implemented and validated the **Inclusion Model** in an open-source Discrete Element Model (DEM) software: LIGGGHTS.
We validated the model against the experimental results of {% cite sunday2024 %}, making this the first experimentally validated magnetic force model for DEM {% cite sikka2026a %}.
Results for Psyche to follow soon. Meanwhile here are some pretty videos :D

<div class="row mt-3" style="overflow-x:auto;white-space:nowrap;">
    <div class="col-sm-4 mt-3 mt-md-0" style="display:inline-block;white-space:normal;">
        <iframe src="https://youtube.com/embed/R4kuxZ1uZNc" title="2.5 mT: Granular Flow" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen
                style="width:100%;aspect-ratio:16/9;border:0;">
        </iframe>
        <div class="caption">
            2.5 mT: Granular Flow
        </div>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0" style="display:inline-block;white-space:normal;">
        <iframe src="https://youtube.com/embed/EfcRUJTKs9I" title="15.0 mT: Correlated Regime" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen
                style="width:100%;aspect-ratio:16/9;border:0;">
        </iframe>
        <div class="caption">
            15.0 mT: Correlated Regime
        </div>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0" style="display:inline-block;white-space:normal;">
        <iframe src="https://youtube.com/embed/DBZdFhMykrs" title="25.0 mT: Plastic Regime" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen
                style="width:100%;aspect-ratio:16/9;border:0;">
        </iframe>
        <div class="caption">
            25.0 mT: Plastic Regime
        </div>
    </div>
</div>
<div class="caption">
        Mass Wasting of Steel Balls in different applied magnetic fields. 
</div>