Documentation Author: Niko Procopi 2019

This tutorial was designed for Visual Studio 2017 / 2019
If the solution does not compile, retarget the solution
to a different version of the Windows SDK. If you do not
have any version of the Windows SDK, it can be installed
from the Visual Studio Installer Tool

Welcome to the Basic OBJ Ray Tracing Tutorial!
Prerequesites: Ray Tracing Compute Animation, OBJ Loaders

In this tutorial, we write an OBJ loader for Ray Tracing
We increase the number of MAX_MESHES to 3, for one plane, one cube, and one car.
This increase needs to be made in main.cpp, and the shaders. We need to call glDispatch
for all the triangles in the scene, in FragmentShader.glsl, one small change was that 
"reflection" is multiplied by the color of the polygon, which is what it should have been all along.
Each face still has only one normal. This is calculated by averaging the normals of the three
vertices in the triangle. In the next tutorial, each vertex will have their own normal, and each pixel
will have an interpolation of the three normals, allowing the car to look more smooth, and less
polygonal. We will also eventually be adding textures, specular maps, and normal maps

