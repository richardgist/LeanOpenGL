cmake_minimum_required(VERSION 3.14)
project(LearnOpengl)

set(CMAKE_CXX_STANDARD 14)

add_subdirectory(extern/glfw)
add_executable(LearnOpengl main.cpp src/glad.c Shader.cpp Shader.h stb_image.h)
target_include_directories(LearnOpengl PUBLIC include)
target_include_directories(LearnOpengl PUBLIC ${OPENGL_INCLUDE_DIR})
target_link_libraries(LearnOpengl PUBLIC glfw ${OPENGL_LIBRARIES})

#target_include_directories(LearnOpengl PUBLIC ${OPENGL_INCLUDE_DIR})

#link_directories("C:/Users/Administrator/CLionProjects/LearnOpengl/lib")
#target_link_libraries(LearnOpengl PUBLIC "C:/Users/Administrator/CLionProjects/LearnOpengl/lib/glfw3.lib" ${OPENGL_LIBRARIES})
#target_link_libraries(LearnOpengl PUBLIC "glfw3.lib" ${OPENGL_LIBRARIES})