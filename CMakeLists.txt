project(testcase)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
include_directories(glfw-3.1.1/include/)

find_package(OpenGL)

set(SOURCES main.cpp GL/gl3w.c)

add_subdirectory(glfw-3.1.1)
add_subdirectory(kiui)

add_executable(foo ${SOURCES})
target_link_libraries(foo kiui ${OPENGL_LIBRARIES} glfw)
