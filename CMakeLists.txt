cmake_minimum_required(VERSION 3.8)
project(visualizer)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(visualizer 
    src/visualizer.cpp)

add_executable(serialization_test
    src/serialization_test.cpp)

target_link_libraries(visualizer ${OPENGL_LIBRARIES} glfw)
target_include_directories(visualizer PUBLIC include)
target_include_directories(serialization_test PUBLIC include)

install(TARGETS
  visualizer
  serialization_test
  DESTINATION lib/${PROJECT_NAME})
