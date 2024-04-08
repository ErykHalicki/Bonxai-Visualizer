cmake_minimum_required(VERSION 3.8)
project(bonxai-viz)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(bonxai-viz 
    src/visualizer.cpp)

add_executable(serialization_test
    src/serialization_test.cpp)

target_link_libraries(bonxai-viz ${OPENGL_LIBRARIES} glfw)
target_include_directories(bonxai-viz PUBLIC include)
target_include_directories(serialization_test PUBLIC include)

install(TARGETS
  bonxai-viz
  bonxai-viz-serialization-test
  DESTINATION bin)
