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

## 5. Cameras and Rendering

A **camera** determines the viewpoint from which a 3D scene is displayed.

Moving or rotating the camera changes what the viewer sees, even if the objects stay in the same place.

**Rendering** is the process of producing a 2D image from a 3D scene using information such as:

- 3D geometry,
- materials,
- lighting,
- and the camera viewpoint.


A video game may render new images continuously as the player moves through a 3D environment. 
[world and camera coordinates](https://leeyngdo.github.io/blog/computer-graphics/2024-02-29-graphics-pipeline/)


---

## Summary

**3D graphics** represent objects using three dimensions: width, height, and depth.

**Meshes** are commonly built from vertices, edges, and faces.

**Transformations** move, rotate, and resize objects in 3D space.

**Materials and lighting** influence how surfaces appear.

**Cameras and rendering** determine how a 3D scene becomes a visible image.

Together, these concepts form the foundation of 3D modeling and graphics used in games and digital media.

---

# In-Class Practice — Build a Simple 3D Scene

Use a beginner-friendly 3D application such as **Tinkercad** (in a web browser) or **Blender** (if already installed).

Create a small scene using basic 3D shapes. For example, build a simple robot, a house, or a game obstacle.

Your scene should include:

1. At least **three 3D primitives** (such as cubes, spheres, or cylinders).
2. At least **one translated object** (moved to a different position).
3. At least **one rotated or scaled object**.
4. At least **two different colors or materials**.
5. A view that clearly shows the scene's **depth**.

### Suggested Steps

1. Open the 3D application and start a new design.
2. Add a cube, sphere, or cylinder.
3. Add at least two more shapes.
4. Move the shapes along different axes.
5. Resize or rotate one shape.
6. Change the colors or materials of at least two objects.
7. Orbit the view to inspect the scene from different angles.
8. Save your project and capture a screenshot of the finished scene.

> The goal is not to build a detailed model. The goal is to understand how basic shapes and transformations work in 3D space.
