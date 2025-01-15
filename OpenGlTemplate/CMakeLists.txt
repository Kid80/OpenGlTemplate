# CMakeList.txt : CMake project for OpenGlTemplate, include source and define
# project specific logic here.
#

# Add source to this project's executable.
add_executable (OpenGlTemplate "OpenGlTemplate.cpp" "OpenGlTemplate.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET OpenGlTemplate PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
