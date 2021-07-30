# Vulkan & OpenGL CAD Mesh Shader Sample

In drawmeshlet.mesh.glsl, ceil division is used to get a number of loop runs from number of vertex/primitive in a meshlet and local workgroup size.
In computeTasksCount function in nvmeshlet_builder.hpp, the number of task shader workgroups to dispatch is calculated from a number of meshlets and a number of meshlet per task.

From:
https://github.com/nvpro-samples/gl_vk_meshlet_cadscene

About mesh shader:
https://www.khronos.org/registry/OpenGL/extensions/NV/NV_mesh_shader.txt
https://github.com/KhronosGroup/GLSL/blob/master/extensions/nv/GLSL_NV_mesh_shader.txt

## Commands to get a list of lines that do ceil division

```
git clone --depth 1 https://github.com/nvpro-samples/gl_vk_meshlet_cadscene.git
cd gl_vk_meshlet_cadscene
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+" > x_y-1_div_y
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+\) / [[:alnum:]_.]+" > x_n-1_div_n
```
