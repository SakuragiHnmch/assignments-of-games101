cmake_minimum_required(VERSION 3.10)
project(Rasterizer)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenCV REQUIRED)
find_package(Eigen3 REQUIRED)


include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(/usr/local/cellar/opencv/4.5.1_2/include/opencv4)

add_executable(Rasterizer main.cpp rasterizer.hpp rasterizer.cpp Triangle.hpp Triangle.cpp)
target_link_libraries(Rasterizer ${OpenCV_LIBS} Eigen3::Eigen)
