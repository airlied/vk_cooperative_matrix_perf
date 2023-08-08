
vk_cooperative_matrix_perf is a sample/benchmark demonstrating performance of
using the VK_KHR_cooperative_matrix Vulkan extension, and the associated
GL_KHR_cooperative_matrix GLSL extension. It is forked from [Jeff Bolz's
original version](https://github.com/jeffbolznv/vk_cooperative_matrix_perf)
for the NVIDIA extensions.

The benchmark queries the supported matrix multiply sizes and precisions from
the Vulkan implementation, and runs a couple different shaders at various
tiles sizes and reports the performance in teraflops. All matrices are
row-major in memory.

Running this application requires an implementation that supports the
VK_KHR_cooperative_matrix extension. At the very least, NVIDIA Turing and AMD
7000 series GPUs, with recent drivers, should have the required support.

Modifying and rebuilding the shaders requires a
[glslangValidator.exe](https://github.com/KhronosGroup/glslang) with
GL_KHR_cooperative_matrix support. During development of this program, glslang
commit
[34d4f78f](https://github.com/KhronosGroup/glslang/commit/34d4f78f03b32960a4e94419ea1c58613726d159)
(Fix interaction between GL_EXT_mesh_shader and GL_EXT_fragment_shading_rate)
was used.

To build the main program, recent [Vulkan
headers](https://github.com/KhronosGroup/Vulkan-Headers) are needed. During
development of this program, Vulkan headers
[450ead1](https://github.com/KhronosGroup/Vulkan-Headers/commit/450ead1)
(Update for Vulkan-Docs 1.3.261) was used.
