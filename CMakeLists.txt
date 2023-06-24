cmake_minimum_required(VERSION 3.20)
project(cimguizmo)

set (CMAKE_CXX_STANDARD 11)

add_library(cimguizmo SHARED
    ../cimgui/imgui/imgui.cpp
    ../cimgui/imgui/imgui_draw.cpp
    ../cimgui/imgui/imgui_demo.cpp
    ../cimgui/imgui/imgui_widgets.cpp
	../cimgui/imgui/imgui_tables.cpp
    cimguizmo.cpp
    imguizmo/imguizmo.cpp)

target_include_directories(cimguizmo PUBLIC ../cimgui)
target_include_directories(cimguizmo PUBLIC ../cimgui/imgui)
set_target_properties(cimguizmo PROPERTIES PREFIX "")