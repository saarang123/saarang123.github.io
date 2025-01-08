---
layout: page
title: Mesh Simplification for 3D Pathfinding
description: Optimizing pathfinding algorithms in robotics through mesh simplification
img: assets/img/mesh.png
importance: 3
category: work
---

# Mesh Simplification for 3D Pathfinding in Robotics

## Project Overview
Developed an advanced 3D pathfinding system optimized through mesh simplification, addressing the critical challenge in robotics where computational efficiency meets navigational accuracy. Our framework combines sophisticated mesh preprocessing with state-of-the-art pathfinding algorithms to achieve significant performance improvements while maintaining path quality.

## Technical Implementation

### Mesh Processing
- Implemented multiple mesh simplification algorithms:
  - Quadratic Error Metrics (QEM) for vertex pair contraction
  - Edge collapse with topology preservation
  - Vertex clustering for rapid simplification
- Varied simplification constants (50%, 75% reductions) to analyze performance trade-offs
- Developed preprocessing tools using Blender and PyVista APIs
- Preserved critical navigational features while reducing geometric complexity

### Motion Planning
- Integrated multiple pathfinding approaches:
  - A* with custom heuristics for 3D navigation
  - RRT (Rapidly-exploring Random Trees) with dynamic step sizing
  - Bi-directional RRT* for optimal path finding
- Added collision detection using spatial hashing:
  - KDTrees and BallTrees for efficient spatial queries
  - Multi-resolution collision checking
- Implemented path smoothing and optimization post-processing

## Performance Results
Our framework achieved significant improvements in computational efficiency:
- 30% reduction in computation time through:
  - Spatial indexing for rapid nearest neighbor queries
  - Multi-resolution mesh representation
  - Parallel processing for collision checking
- Maintained path accuracy with less than 6% deviation in path length
- 35% reduction in memory usage during pathfinding operations
- Successfully benchmarked across different simplification levels

{% include figure.liquid loading="eager" path="assets/img/c.png" title="Path Comparison" class="img-fluid rounded z-depth-1" %}
*Comparison of pathfinding results on original (left) vs simplified (right) meshes showing preserved path quality with reduced computational overhead*

## Tools and Technologies
- Python for core implementation
- Blender and PyVista for mesh processing
- NumPy and SciPy for computational geometry
- OpenGL for 3D visualization
- Custom spatial data structures for optimization

[GitHub Repository](https://github.com/Ashleyjv/MeshSimplification)