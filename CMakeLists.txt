cmake_minimum_required(VERSION 3.16)
project(imgui-template)

add_subdirectory(imgui-1.89.8)


add_executable(win src/win/main.cpp)
target_link_libraries(win PUBLIC imgui imgui-win32 imgui-dx12)


add_executable(unix src/unix/main.cpp)
target_link_libraries(unix  imgui imgui-glfw imgui-opengl3)

