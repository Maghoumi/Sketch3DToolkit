include_directories(${GLEW_INCLUDE_DIR})
add_definitions(-DGLEW_BUILD)
add_library(glew SHARED src/glew.c include/GL/glew.h include/GL/wglew.h)
find_package(OpenGL REQUIRED)
target_link_libraries(glew ${OPENGL_LIBRARIES})
