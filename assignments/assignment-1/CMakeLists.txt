# include libraries
include_directories(../../3rd/eigen3)
#include_directories(../../3rd/opencv/include)
include_directories(${OpenCV_INCLUDE_DIRS})

# executable
include_directories(include)
find_package(OpenCV REQUIRED)
aux_source_directory(src SOURCES)
add_executable(Rasterizer ${SOURCES})
target_link_libraries(Rasterizer eigen ${OpenCV_LIBS})