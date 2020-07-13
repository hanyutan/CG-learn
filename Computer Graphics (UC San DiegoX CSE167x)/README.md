## Computer Graphics 

需要补充OpenGL、GLSL背景知识，会用到它们写代码
需要补充raytracing背景知识

### 概述

**3D Graphics Pipeline:**

Modeling - Animation - Rendering (light & shadow & shading)

**About homework:**

HW1: transformations

HW2: Scene Viewer (GLSL, rasterize)

HW3: Ray Tracer

**Rasterization** essentially goes through all the geometric primitives and dertermines where in the screen they should go.

**Raytracing** does the opposite thing which goes to each point or each pixel in the screen and determines which geometric primitive that corresponds to.

**发展历程介绍**

Rendering: 1970s (lighting)

- Diffuse Lighting (Gouraud 1971)
  
Gouraud shading / smooth shading
  
让阴影更加平滑（still used in OpenGL）
  
- Specular Lighting (Phong 1974) 

  Phong shading / Phong illumination

  让物体显得有光泽 （still used in 99% of computer generated imagery）

- Curved Surfaces, Texture (Blinn 1974)

- Z-Buffer Hidden Surface (Catmull 1974)

Rendering: 1980s, 90s (Global Illumination)

- recursive ray-tracing algorithm (Whitted 1980)

- radiosity (Goral, Torrance et al/ 1984)

  举例：Cornell Box，盒子的颜色都是由墙面反射得到的

- rendering equation (Kajiya 1986)



**History of Computer Animation**

https://www.youtube.com/watch?v=LzZwiLUVaKg

https://www.youtube.com/watch?v=S3hqS6JlKEc





























