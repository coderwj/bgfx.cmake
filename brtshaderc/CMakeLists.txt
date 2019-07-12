cmake_minimum_required(VERSION 3.0)
project (brtshaderc)

include( ../cmake/3rdparty/fcpp.cmake )
include( ../cmake/3rdparty/glsl-optimizer.cmake )
include( ../cmake/3rdparty/glslang.cmake )

add_library( brtshaderc
	brtshaderc.h
    brtshaderc.cpp
)

target_link_libraries( brtshaderc
    bx
    bimg
    bgfx-vertexdecl
    bgfx-shader-spirv
    fcpp
    glsl-optimizer
    glslang
)

target_include_directories(brtshaderc PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})