---
layout: page
title: Discrete mechanics and optimal control techniques applied to a reentry launch vehicle
description: Masters Thesis
img:
importance: 3
category: []
---



I worked with Prof. Ravi Banavar for my masters thesis to to develop an optimal control strategy during glide reentry of a launch vehicle with both state and control constraints. Specifically, I am compared two approaches to solve the optimal control problem. One deals with the use of available open-source optimization tools (CasADi), while the other is to compute the necessary conditions using Discrete-time Maximum Principles (DMP). While open-source tools can provide solutions without diving into the mathematics of the problem, they take considerable efforts to set them up for your problem. On the other hand, with all control actions implemented in discrete-time, DMP can incorporate inequality constraints and provide the first-order necessary conditions for optimality.