---
layout: default
title: "Introduction to 3D Graphics & Modeling"
lesson: 8
---

# Introduction to 3D Graphics & Modeling

In previous lessons, we worked with **2D graphics**, including shapes, typography, layouts, and motion.

**3D graphics** add a third dimension, allowing designers to create objects that have **width, height, and depth**.

3D graphics are used in video games, animation, films, product visualization, and virtual environments.

This lesson introduces the basic ideas behind creating and displaying 3D objects.

---

## 1. From 2D to 3D

A **2D object** has two dimensions: width and height.

A **3D object** has three dimensions: width, height, and depth.

For example:

- A **square** is a 2D shape.
- A **cube** is a 3D object.
- A **circle** is a 2D shape.
- A **sphere** is a 3D object.

3D objects are positioned using three coordinate axes:

- **X-axis:** Left and right.
- **Y-axis:** A second direction across the 3D space.
- **Z-axis:** The third direction, perpendicular to X and Y.

The exact orientation of these axes depends on the software. In many 3D applications, Z represents height.

<figure>
    <img src="{{ '/assets/images/lesson08/8_1.png' | relative_url }}" alt="Comparison of a square and cube, circle and sphere, with three coordinate axes">
    <figcaption>2D shapes, 3D objects, and the X, Y, and Z axes</figcaption>
</figure>

> A 3D object can be viewed from different angles, while a flat 2D shape does not have physical depth in its geometry.

---

## 2. 3D Models and Meshes

A **3D model** is a digital representation of an object in three-dimensional space.

Many 3D models are built from a **mesh**, which contains:

- **Vertices:** Points in 3D space.
- **Edges:** Lines connecting vertices.
- **Faces:** Surfaces enclosed by edges.

For example, a basic cube mesh has **8 vertices, 12 edges, and 6 faces**.

<figure>
    <img src="{{ '/assets/images/lesson08/8_2.png' | relative_url }}" alt="A cube mesh with a vertex, edge, and face highlighted separately">
    <figcaption>Vertices, edges, and faces of a 3D mesh</figcaption>
</figure>

### Basic 3D Shapes

Designers often begin with simple objects called **primitives**, such as:

- Cube
- Sphere
- Cylinder
- Cone

These shapes can be combined or modified to build more complex models.
<figure>
    <img src="{{ '/assets/images/lesson08/8_6.png' | relative_url }}" alt="These shapes can be combined or modified to build more complex models">

</figure>


> Just as we combined basic vector shapes in Inkscape, we can use simple 3D objects as starting points for modeling.

---

## 3. Transformations in 3D

The transformations you learned in 2D also apply to 3D objects.

- **Translation:** Moves an object to a new position.
- **Rotation:** Turns an object around an axis.
- **Scaling:** Changes an object's size.

In 3D, these changes can happen along or around the **X, Y, and Z axes**.

For example, rotating a cube around the Z-axis produces a different result from rotating it around the X-axis.

<figure>
    <img src="{{ '/assets/images/lesson08/8_3.png' | relative_url }}" alt="Examples of a cube translated, rotated, and scaled in 3D space">
    <figcaption>Translation, rotation, and scaling in 3D</figcaption>
</figure>

> Transformations change an object's position, orientation, or size without necessarily changing its basic mesh structure.

---

## 4. Materials and Lighting

A 3D model needs more than geometry to communicate how an object should look.

A **material** describes the appearance of a surface. It may control properties such as:

- **Color:** The surface's basic color.
- **Roughness:** Whether the surface looks matte or shiny.
- **Metallic appearance:** Whether the surface behaves visually like a metal.

**Lighting** affects how we see the model, including its brightness, highlights, and shadows.

For example, the same sphere can look like plastic or polished metal depending on its material and lighting.

<figure>
    <img src="{{ '/assets/images/lesson08/8_4.png' | relative_url }}" alt="Three spheres with different surface materials and lighting">
    <figcaption>How materials and lighting change the appearance of a 3D object</figcaption>
</figure>

> Geometry defines the shape. Materials and lighting help communicate its visual appearance.

---

## 5. Camera View and Transformation Matrices

A 3D scene contains objects positioned in three-dimensional space. However, a computer screen displays a two-dimensional image.

How does a 3D point become a position on the screen?

A graphics system uses a sequence of **transformations** to convert 3D coordinates into screen coordinates. This process is part of the **graphics rendering pipeline**.

### 5.1 The Transformation Pipeline

A 3D point passes through four main transformations:

1. **Model Transformation:** Positions the object in the 3D world.
2. **View Transformation:** Describes the scene relative to the camera.
3. **Projection Transformation:** Determines how 3D positions are projected for viewing.
4. **Viewport Transformation:** Maps the projected positions to pixels on the screen.

For example, imagine a cube in a video game. The model transformation determines where the cube is placed. The view transformation determines where the cube appears relative to the camera. The projection transformation determines how its depth affects its appearance.

<figure>
    <img src="{{ '/assets/images/lesson08/8_5.png' | relative_url }}" alt="Model, view, projection and viewport transformation pipeline">
    <figcaption>From 3D object coordinates to 2D screen coordinates</figcaption>
</figure>

---

### 5.2 Why Do We Use Matrices?

A **matrix** is a rectangular arrangement of numbers that can represent transformations.

In 3D graphics, matrices are used to:

- Move objects (**translation**).
- Change object size (**scaling**).
- Turn objects around an axis (**rotation**).
- Transform coordinates relative to a camera.
- Project 3D positions for display.

A point in 3D space normally has three coordinates:

$$
p=(x,y,z)
$$

To use translation and other transformations consistently with matrices, we introduce an additional coordinate called **w**.

$$
p=
\begin{bmatrix}
x\\
y\\
z\\
1
\end{bmatrix}
$$

This representation is called **homogeneous coordinates**.

We can now use a **4 × 4 matrix** to transform a 3D point.

> **Remember:** A 3D point is represented using four values $(x,y,z,1)$ when applying these transformation matrices.

---

### 5.3 Translation Matrix — Moving an Object

Translation changes the position of an object without changing its size or orientation.

The translation matrix is:

$$
T=
\begin{bmatrix}
1&0&0&t_x\\
0&1&0&t_y\\
0&0&1&t_z\\
0&0&0&1
\end{bmatrix}
$$

Where:

- $t_x$ is movement along the X-axis.
- $t_y$ is movement along the Y-axis.
- $t_z$ is movement along the Z-axis.

**Example**

Suppose a point is located at:

$$
p=
\begin{bmatrix}
1\\2\\3\\1
\end{bmatrix}
$$

We want to move it by $(2,1,0)$.

$$
T=
\begin{bmatrix}
1&0&0&2\\
0&1&0&1\\
0&0&1&0\\
0&0&0&1
\end{bmatrix}
$$

Multiplying the matrix by the point gives:

$$
Tp=
\begin{bmatrix}
3\\3\\3\\1
\end{bmatrix}
$$

The new position is **(3, 3, 3)**.

> Translation adds movement values to the original coordinates.

---

### 5.4 Scaling Matrix — Changing Object Size

Scaling changes the size of an object along one or more axes.

$$
S=
\begin{bmatrix}
s_x&0&0&0\\
0&s_y&0&0\\
0&0&s_z&0\\
0&0&0&1
\end{bmatrix}
$$

Where $s_x$, $s_y$, and $s_z$ are the scaling factors.

- A factor of **1** keeps the original size.
- A factor greater than **1** enlarges the object.
- A factor between **0 and 1** reduces its size.

**Example**

If a point is $(2,1,3)$ and we scale every coordinate by 2:

$$
S=
\begin{bmatrix}
2&0&0&0\\
0&2&0&0\\
0&0&2&0\\
0&0&0&1
\end{bmatrix}
$$

The result is:

$$
Sp=
\begin{bmatrix}
4\\2\\6\\1
\end{bmatrix}
$$

> Scaling multiplies each coordinate by its corresponding scaling factor.

---

### 5.5 Rotation Matrix — Turning an Object

Rotation changes the orientation of an object around an axis.

In 3D graphics, objects can rotate around the **X, Y, or Z axis**.

For rotation around the Z-axis:

$$
R_z(\theta)=
\begin{bmatrix}
\cos\theta&-\sin\theta&0&0\\
\sin\theta&\cos\theta&0&0\\
0&0&1&0\\
0&0&0&1
\end{bmatrix}
$$

Where $\theta$ is the rotation angle.

**Example: Rotate a point by 90° around the Z-axis.**

Recall:

$$
\cos90^\circ=0,\qquad \sin90^\circ=1
$$

Therefore:

$$
R_z(90^\circ)=
\begin{bmatrix}
0&-1&0&0\\
1&0&0&0\\
0&0&1&0\\
0&0&0&1
\end{bmatrix}
$$

Applying this to the point $(1,0,0)$ produces:

$$
R_z
\begin{bmatrix}
1\\0\\0\\1
\end{bmatrix}
=
\begin{bmatrix}
0\\1\\0\\1
\end{bmatrix}
$$

The point moves from **(1, 0, 0)** to **(0, 1, 0)**.

---

### 5.6 Model and View Matrices

The translation, scaling, and rotation matrices can be combined into a **Model Matrix (M)**.

The model matrix transforms a point from its local object coordinates into world coordinates.

$$
p_{world}=Mp_{local}
$$

The **View Matrix (V)** then transforms the world coordinates into camera coordinates.

$$
p_{camera}=Vp_{world}
$$

Combining both:

$$
p_{camera}=VMp_{local}
$$

The view matrix describes the world from the camera's position and orientation.

For example, moving the camera to the right makes a stationary object appear farther to the left in the camera's view.

> **Important:** Matrix multiplication order matters. Changing the order of transformations can change the result.

---

### 5.7 Projection — From 3D to 2D

After the view transformation, the graphics system applies a **Projection Matrix (P)**.

There are two common projection types:

**Perspective Projection**

Objects farther from the camera appear smaller. This creates a realistic sense of depth, similar to human vision.

**Orthographic Projection**

Object size does not decrease with distance. This is useful for technical drawings, diagrams, and some game styles.

<figure>
    <img src="{{ '/assets/images/lesson08/8_7.png' | relative_url }}" alt="Perspective versus orthographic projection of cubes">
    <figcaption>Perspective and orthographic projection</figcaption>
</figure>

The combined transformation is:

$$
p_{clip}=PVMp_{local}
$$

Here:

- **M** = Model Matrix
- **V** = View Matrix
- **P** = Projection Matrix

For perspective projection, the resulting coordinates are divided by their homogeneous $w$ value to obtain normalized device coordinates. A viewport transformation then maps these coordinates to screen pixels.

> Remember the order: **Model → View → Projection → Viewport**.

---

### What Should You Memorize?

1. Explain the purpose of the **Model, View, and Projection matrices**.
2. Recognize the **4 × 4 translation, scaling, and Z-axis rotation matrices**.
3. Apply simple translation and scaling matrices to a point.
4. Calculate a simple 90° rotation around the Z-axis.
5. Explain the difference between **perspective and orthographic projection**.
6. Remember the transformation order: **Model → View → Projection → Viewport**.


### Quick Practice

**Question 1:** A point is at $(2,3,1)$. Translate it by $(1,-2,4)$. What is the new position?

**Question 2:** A point is at $(1,2,3)$. Scale it by $(2,2,2)$. What is the new position?

**Question 3:** Which matrix changes an object's position without changing its size?

**Question 4:** Which projection makes distant objects appear smaller?

**Question 5:** Put these transformations in the correct order: Projection, Model, View.

---

### Further Reading

For a more detailed mathematical explanation, see:

[Youngdo Lee — Graphics Rendering Pipeline](https://leeyngdo.github.io/blog/computer-graphics/2024-02-29-graphics-pipeline/)

---

## Summary

**3D graphics** represent objects using three dimensions: width, height, and depth.

**Meshes** are commonly built from vertices, edges, and faces.

**Transformations** move, rotate, and resize objects in 3D space.

**Materials and lighting** influence how surfaces appear.

**Cameras and rendering** determine how a 3D scene becomes a visible image.

Together, these concepts form the foundation of 3D modeling and graphics used in games and digital media.

---

# In-Class Practice — From 2D to 3D

In this activity, you will explore the difference between **3D-looking drawings** and **real 3D models**.

## Part A — Create a 3D Box in Inkscape

Open [Inkscape](https://inkscape.org/) and create a new document.

1. Select the **3D Box Tool** (`X`).
2. Click and drag to create a 3D-looking box.
3. Adjust the perspective using the tool's handles.
4. Change the colors of the visible faces to create a sense of depth.
5. Save your drawing as an **SVG** file.

> Inkscape creates the appearance of a 3D object using 2D vector graphics.

## Part B — Explore a Real 3D Scene

Choose **one** of the following applications:

- **[Blender](https://www.blender.org/download/)** — Free desktop software for 3D modeling and animation.
- **[Unity Studio](https://unity.com/products/unity-studio)** — A browser-based 3D creation tool. Account access or a trial may be required.

### Your Task

Create a small 3D scene using basic shapes. For example, build a simple robot, a house, or a game obstacle.

Your scene should include:

1. At least **three 3D primitives** (cubes, spheres, or cylinders).
2. At least **one translated object** (moved to a different position).
3. At least **one rotated or scaled object**.
4. At least **two different colors or materials**.

### Suggested Steps

1. Open your chosen application and create a new scene.
2. Add a cube, sphere, or cylinder.
3. Add at least two more 3D shapes.
4. Move the objects along the X, Y, or Z axes.
5. Resize or rotate at least one object.
6. Apply two different colors or materials.
7. Orbit the camera view to inspect your scene from different angles.
8. Save your project and take a screenshot of the finished scene.

### Submission

Submit:

- A **screenshot** of **Inkscape** results from Part A.
- A **screenshot** of your 3D scene from Part B.

