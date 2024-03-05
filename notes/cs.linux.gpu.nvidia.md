---
id: gifvyk24oehjtxf42gimji8
title: Nvidia
desc: ''
updated: 1709455127685
created: 1709450201399
---

*Install `envycontrol` from AUR*
- https://github.com/bayasdev/envycontrol
## Check which drivers are running ?
```bash
$ envycontrol --query
hybrid
```
## Change graphics card to integrated
```bash
$ sudo envycontrol -s integrated
[sudo] password for hg: 
Switching to integrated mode
Successfully disabled nvidia-persistenced.service
Rebuilding the initramfs...
Successfully rebuilt the initramfs!
Operation completed successfully
Please reboot your computer for changes to take effect!
```

> Note: *External screen* won't work with this in Asus TUF (it could be that HDMI output is using Nvidia GPU)

## Check if particular graphic card is being used ?

### When only nvidia is on and integrated is off

```bash
$ glxinfo | grep NVIDIA
server glx vendor string: NVIDIA Corporation
client glx vendor string: NVIDIA Corporation
OpenGL vendor string: NVIDIA Corporation
OpenGL renderer string: NVIDIA GeForce RTX 3050 Ti Laptop GPU/PCIe/SSE2
OpenGL core profile version string: 4.6.0 NVIDIA 545.29.06
OpenGL core profile shading language version string: 4.60 NVIDIA
OpenGL version string: 4.6.0 NVIDIA 545.29.06
OpenGL shading language version string: 4.60 NVIDIA
OpenGL ES profile version string: OpenGL ES 3.2 NVIDIA 545.29.06
```

```bash
$ glxinfo | grep -i amd
    GL_AMD_multi_draw_indirect, GL_AMD_seamless_cubemap_per_texture, 
    GL_AMD_vertex_shader_layer, GL_AMD_vertex_shader_viewport_index, 
    GL_AMD_multi_draw_indirect, GL_AMD_seamless_cubemap_per_texture, 
    GL_AMD_vertex_shader_layer, GL_AMD_vertex_shader_viewport_index, 
```


> **Imp:** `hybrid` mode works the best, even pure nvidia is having slight stutters

### When hybrid mode is activated
```bash
$ glxinfo | grep -i amd
    Vendor: AMD (0x1002)
    Device: AMD Radeon Graphics (radeonsi, rembrandt, LLVM 16.0.6, DRM 3.57, 6.7.6-arch1-1) (0x1681)
OpenGL vendor string: AMD
OpenGL renderer string: AMD Radeon Graphics (radeonsi, rembrandt, LLVM 16.0.6, DRM 3.57, 6.7.6-arch1-1)
    GL_AMD_conservative_depth, GL_AMD_depth_clamp_separate, 
    GL_AMD_draw_buffers_blend, GL_AMD_framebuffer_multisample_advanced, 
    GL_AMD_gpu_shader_int64, GL_AMD_multi_draw_indirect, 
    GL_AMD_performance_monitor, GL_AMD_pinned_memory, 
    GL_AMD_query_buffer_object, GL_AMD_seamless_cubemap_per_texture, 
    GL_AMD_shader_stencil_export, GL_AMD_shader_trinary_minmax, 
    GL_AMD_texture_texture4, GL_AMD_vertex_shader_layer, 
    GL_AMD_vertex_shader_viewport_index, GL_ANGLE_texture_compression_dxt3, 
    GL_AMD_conservative_depth, GL_AMD_depth_clamp_separate, 
    GL_AMD_draw_buffers_blend, GL_AMD_framebuffer_multisample_advanced, 
    GL_AMD_multi_draw_indirect, GL_AMD_performance_monitor, 
    GL_AMD_pinned_memory, GL_AMD_query_buffer_object, 
    GL_AMD_seamless_cubemap_per_texture, GL_AMD_shader_stencil_export, 
    GL_AMD_shader_trinary_minmax, GL_AMD_texture_texture4, 
    GL_AMD_vertex_shader_layer, GL_AMD_vertex_shader_viewport_index, 
    GL_AMD_framebuffer_multisample_advanced, GL_AMD_performance_monitor, 
```

```bash
$ glxinfo | grep -i nvidia
```

> Q : Is nvidia not being used in hybrid mode ? But the performance is better than that of only *nvidia* mode
> - The memory shown in system monitor is also just 100 mb when using hybrid
> - Could it be that in hybrid the only use of nvidia gpu is to display on screen of external monitor

---

