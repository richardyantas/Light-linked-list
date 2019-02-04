cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_STANDARD 11)
project(main)

find_package(PkgConfig REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
pkg_search_module(GLFW REQUIRED glfw3)

include_directories(${OPENGL_INCLUDE_DIR} ${GLFW_INCLUDE_DIR} app/include /include/glad)

set(HEADERS app/include/LUtils.h)
set(SOURCES app/src/main.cpp app/src/LGlad.cpp app/src/LUtils.cpp)

add_executable(main  ${HEADERS} ${SOURCES} )
target_link_libraries(main glfw dl ${OPENGL_LIBRARY} ${GLFW_LIBRARY} ${OpenCV_LIBS} )