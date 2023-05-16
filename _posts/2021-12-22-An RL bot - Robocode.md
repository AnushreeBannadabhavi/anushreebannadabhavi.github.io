---
layout: post
title: An RL bot - Robocode
subtitle: Reinforcement Learning agent built with Java
tags: [Reinforcement Learning, NeuralNet, Java]
---

Built a robocode tank (a Reinforcement Learning agent) that battles with another robot (an enemy) and defeats it ~80% of the time. The error backpropagation algorithm as applied to multi-layer perceptron and reinforcement learning is used for the robot’s attack or defence strategy.

<style>
.video-container {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
}

.video-container video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>

### Before training the battle looks something like this:
- Yellow battle tank : Opponent
- Blue battle tank : My battle tank (Not trained)

<div class="video-container">
  <video controls>
    <source src="/assets/img/robocode-before.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

### After training:
- Yellow battle tank : Opponent
- Blue battle tank : My battle tank (Trained)

<div class="video-container">
  <video controls>
    <source src="/assets/img/robocode-after.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>


[GitHub](https://github.com/AnushreeBannadabhavi/Reinforcement-Learning-Neural-Net---Robocode)