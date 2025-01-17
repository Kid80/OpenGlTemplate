# CMakeList.txt : CMake project for OpenGlTemplate, include source and define
# project specific logic here.
#

# Add source to this project's executable.
add_executable (OpenGlTemplate "main.cpp" "shaders.h")

target_link_libraries(OpenGlTemplate PRIVATE glad)
target_link_libraries(OpenGlTemplate PRIVATE glfw)
target_link_libraries(OpenGlTemplate PRIVATE glm)

b_embed(OpenGlTemplate Runtime/main.vert)
b_embed(OpenGlTemplate Runtime/main.frag)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET OpenGlTemplate PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
