---
layout: default
title: "Foundations of Digital Graphics"
lesson: 1
---

# Foundations of Digital Graphics

Digital graphic design is not defined by a particular software package.

Applications such as Inkscape, Adobe Illustrator, and other graphics editors
provide different interfaces and tools, but many of the underlying concepts
remain the same.

In this course, we will focus on understanding those concepts first and then
use graphics software to apply them.

> **Classroom software:** Inkscape  
> **Alternative software:** Students may use another suitable vector graphics
> editor, such as Adobe Illustrator.

---

## Learning Outcomes

By the end of this lesson, you should be able to:

- distinguish between raster and vector graphics;
- explain when raster or vector graphics are more appropriate;
- identify points, lines, and planes as fundamental elements of visual form;
- explain the basic idea of a vector path;
- distinguish between a fill and a stroke;
- create and transform simple vector objects;
- export graphics in appropriate raster and vector formats.

---

# 1. How Can a Computer Represent an Image?

A computer needs a way to represent visual information.

Two important approaches are:

1. **Raster graphics**
2. **Vector graphics**

Although both can produce images that look similar on a screen, they represent
those images in fundamentally different ways.

---

# 2. Raster Graphics

A **raster graphic** is constructed from a grid of small picture elements
called **pixels**.

Each pixel stores information about its appearance, such as its color.

Digital photographs are a common example of raster graphics.

The amount of pixel information available determines the resolution of the
image. When a raster image is enlarged significantly, the individual pixels
may become visible and the image may lose apparent sharpness.

### Common raster formats

- JPEG / JPG
- PNG
- GIF
- TIFF

### Raster graphics are particularly useful for:

- photographs;
- detailed textures;
- scanned images;
- images containing complex variations in color.

---

# 3. Vector Graphics

A **vector graphic** represents an image using geometrically defined objects.

These objects may include:

- points;
- lines;
- curves;
- paths;
- geometric shapes;
- fills;
- strokes.

Instead of storing the color of every individual pixel, a vector file stores
information describing the objects that form the graphic.

For example, a circle can be described using properties such as its position,
size, fill, and outline.

Because its geometry can be recalculated at different sizes, vector artwork can
usually be enlarged without the pixelation associated with raster graphics.

### Common vector formats

- SVG
- EPS

PDF files may also contain vector graphics, raster graphics, or a combination
of both.

### Vector graphics are particularly useful for:

- logos;
- icons;
- diagrams;
- illustrations;
- interface elements;
- typography and other scalable artwork.

---

# 4. Raster vs. Vector

| Property | Raster | Vector |
|---|---|---|
| Representation | Pixels | Geometric objects and paths |
| Resolution dependent | Yes | Generally no |
| Enlarging | May reveal pixels | Geometry remains scalable |
| Suitable for | Photos and complex imagery | Logos, icons, diagrams and illustrations |
| Examples | JPG, PNG, TIFF | SVG, EPS |

Neither representation is always better.

The appropriate representation depends on the type of graphic and how it will
be used.

---

# 5. Point, Line and Plane

One way to understand graphic form is to begin with three fundamental visual
elements:

**Point → Line → Plane**

These simple elements can be combined and transformed to create much more
complex visual compositions.

## Point

A **point** marks a position in space.

A single point can attract attention and establish a visual location.

When multiple points are introduced, relationships begin to appear between
them through their position, distance, scale, and arrangement.

In vector graphics, points also have a technical role because points or nodes
can define locations along a path.

---

## Line

A **line** creates direction and connection.

Lines can vary in:

- length;
- width;
- direction;
- curvature;
- continuity;
- visual character.

Lines can divide space, connect elements, indicate movement, create boundaries,
or guide the viewer's attention.

In vector graphics, a line can be represented by a **path with a stroke**.

---

## Plane

A **plane** is a two-dimensional surface or shape.

Planes can be geometric, such as circles and rectangles, or irregular and
organic.

In vector graphics, a closed path can define a shape whose interior can be
filled.

Therefore, we can begin connecting visual-design terminology with digital
vector terminology:

| Visual concept | Vector graphics concept |
|---|---|
| Point | Node / anchor point |
| Line | Path / stroke |
| Plane | Closed path / shape |

---

# 6. Paths

A **path** is one of the fundamental structures used in vector graphics.

A path is formed by points connected by segments.

Paths may be:

### Open and Closed paths

An open path has separate starting and ending points. A closed path returns to its starting point and encloses an area.

<figure>
    <img src="{{ '/assets/images/lesson01/1.png' | relative_url }}"
         alt="Comparison">
</figure>

Closed paths are particularly important because their enclosed areas can
receive fills.

Later in the course, we will examine how more complex curved paths can be
constructed and edited using nodes and Bézier curves.

---

# 7. Fill and Stroke

Two important properties of vector objects are **fill** and **stroke**.

## Fill

The fill describes the appearance of the interior of a closed shape.

A fill might use:

- a solid color;
- a gradient;
- a pattern;
- transparency.

## Stroke

The stroke describes the visible appearance of a path.

Stroke properties can include:

- color;
- width;
- line style;
- joins;
- end caps.

Understanding the distinction between the geometry of an object and its
appearance is fundamental to working with vector graphics.
<figure>
    <img src="{{ '/assets/images/lesson01/2.png' | relative_url }}"
         alt="Comparison">
</figure>

---

# 8. Software Is a Tool, Not the Concept

Different vector graphics applications may give the same operation different
names or place it in different menus.

For example, one application may call a point a **node**, while another may
use the term **anchor point**.

The important question is therefore not:

> "Which button should I click?"

but:

> "What operation am I trying to perform?"

Throughout this course, classroom demonstrations will primarily use
**Inkscape**, a free vector graphics editor.

Students may use another suitable vector graphics application when the same
concepts and required outcomes can be demonstrated.

---

# Practical Activity

## Building an Image from Basic Forms

Create a simple vector illustration using basic geometric shapes.

Possible subjects include:

- a robot;
- a house;
- a flower;
- a rocket;
- a simple game character.

Your design should contain:

1. at least three different geometric shapes;
2. different fill colors;
3. a visible stroke on at least two objects;
4. objects of different sizes;
5. objects that have been repositioned and arranged into a recognizable image.

Do not worry about producing a complicated illustration.

The purpose of this exercise is to understand how simple visual elements can
be combined into a larger graphic.

---

# Experiment: Raster vs. Vector

When your illustration is complete:

1. save the editable vector source;
2. export a copy as **SVG**;
3. export another copy as **PNG**;
4. enlarge both exported versions;
5. compare their appearance.

Consider the following question:

> Why does enlarging the two representations produce different results?

---

# Key Takeaways

- Digital images can be represented using raster or vector graphics.
- Raster graphics represent images using pixels.
- Vector graphics represent visual elements geometrically.
- Point, line, and plane provide a basic vocabulary for understanding visual form.
- Vector artwork is constructed using paths and shapes.
- Fill controls the interior appearance of a shape.
- Stroke controls the appearance of a path.
- The concepts of digital graphics are more important than the interface of any
  individual software application.

---

# Further Reading

Ellen Lupton and Jennifer Cole Phillips, *Graphic Design: The New Basics*,
section on **Point, Line, Plane**.

---

*Digital Graphics Foundations*