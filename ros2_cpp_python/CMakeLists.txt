cmake_minimum_required(VERSION 3.8)
project(ros2_cpp_python)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
find_package(Python3 COMPONENTS Interpreter Development)

add_executable(ros2_cpp_python
  src/main.cpp
)

ament_target_dependencies(ros2_cpp_python PUBLIC Python3)

ament_package()
