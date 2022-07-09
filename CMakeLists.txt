cmake_minimum_required(VERSION 3.21)
project(cgalSampleProject)

set(CMAKE_CXX_STANDARD 14)

set(CMAKE_BUILD_TYPE Release)

# Add CGAL to Path
#list(APPEND CMAKE_PREFIX_PATH ${CMAKE_CURRENT_LIST_DIR}/deps/CGAL/lib/cmake/CGAL)
list(APPEND CMAKE_PREFIX_PATH ${CMAKE_CURRENT_LIST_DIR}/deps/CGAL-5.4.1/lib/cmake/CGAL)
set(CMAKE_CXX_STANDARD 14)

# Set data directory
set(CGAL_DATA_DIR CMAKE_CURRENT_BINARY_DIR)

# Find CGAL
find_package(CGAL)

# Include include directories
include_directories(deps/CGAL-5.4.1/include)

add_executable(cgalTest main.cpp)
target_link_libraries(cgalTest CGAL::CGAL)