# An Introduction to Generative Art

Generative art is art programmed using a computer that intentionally introduces randomness, algorithmic design, and autonomy into the creative process. Instead of drawing shapes directly, the artist designs the *system* or ruleset that generates the art.

In this post, we will explore the core concepts of generative art and look at a simple formula to create wave-like visual patterns.

---

## Core Pillars of Generative Art

When writing code to generate visuals, we rely on three main pillars:

### 1. Algorithms & Rules
We write logical steps that define how shapes are positioned, colored, and transformed. For instance, nested loops can draw grids, and recursive functions can grow fractal-like trees.

### 2. Randomness & Noise
True randomness (`random()`) makes things unpredictable. However, natural patterns are rarely completely random. Instead, we use **Perlin Noise** or **Simplex Noise** to create smooth, organic transitions (like mountain ranges, water waves, or wind flow).

### 3. Math & Geometry
Math is the ultimate brush. Trigonometry (Sine and Cosine) is widely used to create circular motions, periodic waves, and natural oscillations.

---

## A Simple Wave Formula

To generate a wave-like curve, we can use the trigonometric sine function:

\[ y = A \cdot \sin(B \cdot x + C) + D \]

Where:
- \( A \) is the **amplitude** (controlling the wave's height).
- \( B \) is the **frequency** (controlling how close the peaks are).
- \( C \) is the **phase shift** (shifting the wave horizontally, useful for animating over time).
- \( D \) is the **vertical shift** (centering the wave).

By changing these parameters dynamically in a loop, we can draw beautiful, flowing ribbons of colors.

---

## Getting Started with p5.js

The easiest way to begin with generative art is **p5.js**, a JavaScript library designed for creative coding. Here is a simple sketch structure to draw a circle that fluctuates:

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(240);
  
  // Center of canvas
  let centerX = width / 2;
  let centerY = height / 2;
  
  // Use sine to animate diameter over time
  let diameter = 200 + sin(frameCount * 0.05) * 50;
  
  fill(120, 180, 240);
  noStroke();
  ellipse(centerX, centerY, diameter, diameter);
}
```

Try pasting this into the online [p5.js Web Editor](https://editor.p5js.org/) to see it in action!

---

*Published on: August 6, 2026*
*Author: Harshit*

[← Back to Home](../README.md)
