cmake_minimum_required(VERSION 2.8.3)
project(catkin_and_catkin_simple)

find_package(catkin_simple REQUIRED)

catkin_simple()

cs_add_library(example_library src/example-library.cc)

cs_add_executable(example_executable src/main.cc)
target_link_libraries(example_executable example_library)

cs_install()

cs_install_scripts(scripts/example_script.py)

cs_export()