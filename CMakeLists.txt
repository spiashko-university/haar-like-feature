cmake_minimum_required(VERSION 3.9)

project(opencv_cardetect)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(OpenCV REQUIRED)
set(SOURCE_FILES cardetect.cpp)
add_executable(opencv_cardetect ${SOURCE_FILES})
include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(opencv_cardetect ${OpenCV_LIBS})

message(STATUS "OpenCV_INCLUDE_DIRS = ${OpenCV_INCLUDE_DIRS}")
message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")

file(COPY CarData DESTINATION .)
file(COPY data DESTINATION .)