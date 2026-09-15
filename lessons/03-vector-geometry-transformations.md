---
layout: default
title: "Vector Geometry & Transformations"
lesson: 3
---

# Vector Geometry & Transformations

In the previous lessons, we introduced vector graphics as geometric objects and explored how points, lines, and planes form visual compositions.

We now move one step further:

> **How can we construct, reshape, combine, and transform vector geometry?**

In this lesson, we will explore **Bézier curves**, **path operations**, and **geometric transformations**.

These concepts are not specific to Inkscape. They describe the geometry behind many operations found in vector graphics software.

---

## Learning Outcomes

By the end of this lesson, you should be able to:

- explain how Bézier curves are controlled;
- reshape vector paths using nodes and handles;
- construct complex shapes from simple geometry;
- distinguish between common Boolean path operations;
- explain translation, scaling, and rotation as geometric transformations;
- understand the importance of proportion when scaling;
- apply these concepts using Inkscape.

---

# 1. From Paths to Curves

In Lesson 1, we introduced a **path** as points connected by segments.

A segment may be straight, but vector graphics also allow us to construct smooth curved paths.

One of the most important mathematical tools for creating these curves is the **Bézier curve**.

Bézier curves are widely used in:

- vector illustrations;
- fonts and typography;
- logos and icons;
- interface graphics;
- animation paths;
- computer-aided design.

Instead of storing every position along a curve individually, the computer can calculate the curve from a small number of **control points**.

---

# 2. Bézier Curves

Consider a simple curve controlled by three points:

- \(P_0\) — starting point
- \(P_1\) — control point
- \(P_2\) — ending point

A quadratic Bézier curve can be described by:

\[
B(t) = (1-t)^2P_0 + 2(1-t)tP_1 + t^2P_2
\]

where:

\[
0 \leq t \leq 1
\]

The value of \(t\) represents a position along the curve.

When:

\[
t=0
\]

the curve begins at \(P_0\).

When:

\[
t=1
\]

the curve reaches \(P_2\).

The position of \(P_1\) influences the shape of the curve between them.

<figure>
    <img src="{{ '/assets/images/lesson03/01-bezier.png' | relative_url }}"
         alt="A simple Bezier curve showing its start point, control point, and end point">
    <figcaption>
        A Bézier curve controlled by a start point, control point, and end point.
    </figcaption>
</figure>

> You do not need to calculate the Bézier equation manually. The important idea is that a curve can be mathematically controlled using a small number of points.

---

## Control Handles

Vector graphics editors provide a visual way to manipulate Bézier geometry.

When editing a curved path, **control handles** can extend from its nodes.

Moving a handle changes:

- the direction in which the curve leaves or approaches a node;
- the amount of curvature;
- the smoothness of the transition.

<figure>
    <img src="{{ '/assets/images/lesson03/02-bezier-handles.png' | relative_url }}"
         alt="Bezier curves changing as their control handles are moved">
    <figcaption>
        Changing the position of control handles changes the geometry of the curve.
    </figcaption>
</figure>

This demonstrates an important relationship between mathematics and graphics software:

> **The software allows us to manipulate mathematical geometry visually.**

---

# 3. Reshaping Paths

A basic geometric object does not have to remain in its original form.

For example, a rectangle begins as a regular geometric shape.

Once it is converted into a **path**, its nodes can be edited individually.

We can then:

- move nodes;
- add nodes;
- remove nodes;
- join or separate nodes;
- convert straight segments into curves;
- adjust Bézier handles.

This means a simple geometric primitive can become a completely custom shape.

### In Inkscape

A shape can be converted using:

**Path → Object to Path**

The **Node Tool** can then be used to manipulate its geometry.

The important distinction is:

**Shape Tool → manipulate the properties of the original shape**

**Node Tool → manipulate the geometry of the resulting path**

---

# 4. Constructing Complex Shapes

Complex vector forms do not always need to be drawn one node at a time.

Instead, we can begin with simple shapes and combine their geometry.

For example:

**Circle + Circle → new shape**

The result depends on the operation we apply.

These operations are commonly called **Boolean operations** or **path operations**.

---

## Union

**Union** combines the areas of two or more objects.

The result becomes one path.

\[
A \cup B
\]

This is useful when several simple shapes should become one larger form.

---

## Difference

**Difference** subtracts one shape from another.

\[
A - B
\]

For example, subtracting one circle from another can produce a crescent shape.

The order of the objects matters because one object is being removed from another.

---

## Intersection

**Intersection** keeps only the area shared by both shapes.

\[
A \cap B
\]

Everything outside the overlapping region is removed.

---

## Exclusion

**Exclusion** removes the overlapping region while keeping the areas that do not overlap.

Conceptually:

\[
(A \cup B) - (A \cap B)
\]

---

## Division

**Division** uses one path to divide another object into separate regions.

Unlike Union, Difference, or Intersection, the purpose is not simply to keep or remove an area. It creates separate editable pieces.

---

<figure>
    <img src="{{ '/assets/images/lesson03/03-boolean-operations.png' | relative_url }}"
         alt="Comparison of union, difference, intersection, exclusion, and division operations">
    <figcaption>
        Different Boolean operations applied to the same starting shapes.
    </figcaption>
</figure>

### Why is this useful?

Imagine creating:

- a crescent from circles;
- a cloud from overlapping circles;
- a game controller from rectangles and circles;
- an icon from several geometric forms.

Instead of drawing a complicated outline manually, we can ask:

> **Can this form be constructed from simpler geometry?**

---

# 5. Geometric Transformations

In the previous lesson, you moved, resized, and rotated objects in Inkscape.

These familiar editing actions are examples of **geometric transformations**.

A transformation changes the coordinates of an object according to a rule.

We will consider three important transformations:

1. translation;
2. scaling;
3. rotation.

<figure>
    <img src="{{ '/assets/images/lesson03/04-transformations.png' | relative_url }}"
         alt="An object shown before and after translation, scaling, and rotation">
    <figcaption>
        Translation, scaling, and rotation applied to the same object.
    </figcaption>
</figure>

---

# 6. Translation

A **translation** changes the position of an object.

Suppose a point is located at:

\[
P=(x,y)
\]

If we move it by \(t_x\) horizontally and \(t_y\) vertically, its new position is:

\[
P'=(x+t_x,\ y+t_y)
\]

For example:

\[
(2,3)\rightarrow(7,5)
\]

The point has moved:

- 5 units horizontally;
- 2 units vertically.

Its position changed, but its **size, shape, and orientation did not**.

In a graphics editor, dragging an object from one location to another is a visual application of translation.

---

# 7. Scaling

**Scaling** changes the size of an object.

For a point:

\[
P=(x,y)
\]

scaling can be represented as:

\[
P'=(s_xx,\ s_yy)
\]

where:

- \(s_x\) controls horizontal scaling;
- \(s_y\) controls vertical scaling.

If:

\[
s_x=s_y
\]

the object is scaled equally in both directions.

For example:

\[
s_x=s_y=2
\]

produces an object that is twice as large.

---

## Proportion

Scaling becomes particularly important in design because changing width and height independently can **distort** an object.

Consider an object with width \(W\) and height \(H\).

Its aspect ratio can be written as:

\[
r=\frac{W}{H}
\]

If the width and height are scaled by the same factor, this ratio remains unchanged.

This is called **proportional scaling**.

<figure>
    <img src="{{ '/assets/images/lesson03/05-proportion.png' | relative_url }}"
         alt="Comparison between proportional and non-proportional scaling">
    <figcaption>
        Proportional scaling preserves the relationship between width and height, while non-proportional scaling can distort the object.
    </figcaption>
</figure>

### In a graphics editor

You will often find an option to **lock the aspect ratio**.

When the ratio is locked, changing one dimension automatically adjusts the other.

This is particularly useful for:

- logos;
- icons;
- photographs;
- characters;
- interface assets.

---

# 8. Rotation

A **rotation** turns an object around a point.

Rotation depends on two important properties:

- the **angle of rotation**;
- the **centre of rotation**.

For a point \((x,y)\) rotated around the origin by an angle \(\theta\):

\[
x'=x\cos\theta-y\sin\theta
\]

\[
y'=x\sin\theta+y\cos\theta
\]

Again, you do not need to calculate this equation manually.

The important idea is:

> Rotation changes the coordinates of the points that construct the object while preserving its basic geometry.

For example, rotating an object by:

\[
\theta=90^\circ
\]

changes its orientation but does not automatically change its size or proportions.

### Centre of Rotation

The same object can produce very different movement depending on where its centre of rotation is located.

A shape may rotate:

- around its own centre;
- around one of its corners;
- around a point outside the object.

This idea becomes particularly useful later in **animation and motion graphics**.

---

# 9. Aligning Objects

Transformations help us manipulate individual objects, but graphics often contain many objects that need to be organised together.

**Alignment** places objects relative to a shared reference.

Objects can be aligned by:

- left edge;
- right edge;
- top edge;
- bottom edge;
- horizontal centre;
- vertical centre.

**Distribution** controls the spacing between several objects.

For example, instead of manually estimating the distance between four icons, we can distribute them so that their spacing is mathematically consistent.

This helps create more precise and organised layouts.

---

# From Mathematics to Inkscape

The terminology used in mathematics and the terminology shown in graphics software are closely related.

| Concept | Inkscape operation |
|---|---|
| Bézier curve | Bézier / Pen Tool |
| Control points | Nodes and handles |
| Reshaping geometry | Node Tool |
| Convert geometry | Object to Path |
| Union | Path → Union |
| Difference | Path → Difference |
| Intersection | Path → Intersection |
| Exclusion | Path → Exclusion |
| Division | Path → Division |
| Translation | Move |
| Scaling | Resize |
| Rotation | Rotate |
| Proportion | Lock aspect ratio |
| Alignment | Align and Distribute |

The interface may change between different graphics applications, but the underlying concepts remain transferable.


---
# In-Class Lab: Create a Simple Vector Leaf
---
In this activity, you will create a simple **leaf icon** while applying the main concepts from this lesson.

<figure>
    <img src="{{ '/assets/images/lesson03/06-lab-leaf.png' | relative_url }}"
         alt="Simple vector leaf created using geometric operations">
    <figcaption>
        Example of a simple vector leaf constructed and transformed in Inkscape.
    </figcaption>
</figure>

## Steps

1. Use the **Bézier/Pen Tool** to draw the basic outline of a leaf.

2. Use the **Node Tool** and Bézier handles to reshape the curves until the leaf has a smooth form.

3. Add a simple shape or path to the leaf and experiment with one **Boolean operation**, such as:
   - Union,
   - Difference, or
   - Intersection.

4. Duplicate your finished leaf.

5. **Scale** one copy while preserving its proportions.

6. **Rotate** another copy to create a small arrangement of leaves.

7. Use **Align and Distribute** to organise your final objects.

8. Save your editable work as an **SVG file**.

---
