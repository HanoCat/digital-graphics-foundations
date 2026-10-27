---
layout: default
title: "Introduction to Motion Graphics"
lesson: 7
---

# Introduction to Motion Graphics

So far, we have designed **shapes, colors, text, and layouts** as still images.

**Motion graphics** bring these visual elements to life by changing their **position, size, rotation, color, or appearance over time**.

Motion can help a designer **attract attention, explain information, and guide the viewer** through a message.

---

## 1. What Are Motion Graphics?

**Motion graphics** are graphic design elements that appear to move or change over time.

Common examples include:

- animated titles and logos,
- moving icons in an application,
- transitions between presentation slides,
- and animated information in videos or games.

Unlike a still poster, a motion graphic uses **time** as part of its design.

<figure>
    <img src="{{ '/assets/images/lesson07/7_1.png' | relative_url }}" alt="Three frames showing a simple circle moving across a page">
    <figcaption>From a still graphic to a moving graphic</figcaption>
</figure>

> Motion should support the message, not simply add decoration.

---

## 2. Frames, Time, and Frame Rate

A motion graphic can be understood as a sequence of **frames**.

A **frame** is one still image in that sequence. When frames are shown quickly, viewers perceive continuous movement.

**Frame rate** describes how many frames are displayed each second. It is often measured in **frames per second (fps)**.

For example, a sequence played at **24 fps** displays 24 frames in one second.

<figure>
    <img src="{{ '/assets/images/lesson07/7_2.png' | relative_url }}" alt="A sequence of frames showing a shape at different positions">
    <figcaption>Individual frames create the appearance of movement</figcaption>
</figure>

The **duration** of an animation is how long it lasts. Timing influences whether movement feels quick, slow, calm, or energetic.

---

## 3. Keyframes and Transitions

A **keyframe** marks an important state of an object at a particular moment.

For example, to move a circle from left to right:

- **First keyframe:** The circle is on the left.
- **Last keyframe:** The circle is on the right.
- **In-between frames:** The circle appears at positions between them.

The process of creating intermediate changes between keyframes is called **interpolation** or **tweening**.

<figure>
    <img src="{{ '/assets/images/lesson07/7_3.png' | relative_url }}" alt="Start and end keyframes with intermediate positions of a circle">
    <figcaption>Keyframes and in-between positions</figcaption>
</figure>

Motion can involve different **transformations**, including:

- **Translation:** Changing position.
- **Scaling:** Changing size.
- **Rotation:** Turning around a point.
- **Opacity:** Changing how transparent an object appears.

These build on the vector transformations explored in earlier lessons.

---

## 4. Timing and Easing

Two animations can start and end in the same places but feel very different because of their timing.

### Linear Motion

An object moves at a **constant speed** between its starting and ending positions.

### Ease-In

An object **starts slowly and speeds up**.

### Ease-Out

An object **starts quickly and slows down**.

### Ease-In-Out

An object **starts slowly, speeds up, and slows down again**.

<figure>
    <img src="{{ '/assets/images/lesson07/7_4.png' | relative_url }}" alt="Comparison of linear, ease-in, ease-out, and ease-in-out movement">
    <figcaption>Different timing patterns change how motion feels</figcaption>
</figure>

> Smooth motion does not always mean slow motion. The important choice is how the speed changes over time.

---

## 5. Motion and Visual Communication

Motion should have a clear purpose within a design.

Designers can use it to:

- **Direct attention:** Reveal the most important element first.
- **Show a change:** Demonstrate how an object moves or transforms.
- **Create continuity:** Connect one visual state to the next.
- **Provide feedback:** Show that a button was pressed or an action was completed.

For example, an icon that becomes larger when selected can help users recognize which option is active.

A **loop** is an animation that repeats. Loops are useful for simple moving icons or repeated visual patterns, but too much repeated motion can become distracting.

<figure>
    <img src="{{ '/assets/images/lesson07/7_5.png' | relative_url }}" alt="Three stages of an animated icon that grows to indicate selection">
    <figcaption>Motion can communicate changes and guide attention</figcaption>
</figure>

Good motion graphics use the same principles as still designs: **contrast, alignment, hierarchy, and simplicity**.

---

## Summary

**Motion graphics** add time and movement to graphic design.

**Frames** are the individual images that create the appearance of movement.

**Keyframes** define important states, while **in-between frames** connect them.

**Timing and easing** control how movement feels.

The goal is not to make everything move. The goal is to use movement **intentionally to communicate clearly**.

---

# In-Class Practice — Designing Motion Frames

Open **Inkscape** and create a new document.

Design a simple **four-frame motion sequence** using a basic vector shape or short word. You may choose a bouncing ball, a moving arrow, or a title that grows larger.

Your sequence should demonstrate:

1. A clear **starting state** and **ending state**.
2. At least **two in-between frames**.
3. A visible change in **position, size, or rotation**.
4. Consistent colors and a simple background.
5. A clear direction or purpose for the motion.

### Suggested Inkscape Steps

1. Draw a rectangle to represent the frame area.
2. Create a circle, arrow, or short word inside it.
3. Duplicate the frame area and its contents three times (`Ctrl + D` for selected objects).
4. Move, resize, or rotate the object slightly in each new frame.
5. Align the four frames in a row so the movement can be compared easily.
6. Add small labels: **Frame 1**, **Frame 2**, **Frame 3**, and **Frame 4**.
7. Save the design as an **SVG** and export a **PNG**.

> Inkscape is being used here to **design the individual frames**, not to play an animation. A separate animation tool would be needed to turn the frames into a moving video or GIF.

The goal is to understand **how visual changes across frames create motion**, rather than to produce a complex animation.
