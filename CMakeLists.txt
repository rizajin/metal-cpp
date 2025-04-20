cmake_minimum_required(VERSION 3.15)

project(metal-cpp LANGUAGES CXX)

add_library(metal-cpp INTERFACE)

target_include_directories(metal-cpp INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(metal-cpp INTERFACE
    "-framework Metal"
    "-framework Foundation"
    "-framework QuartzCore"
    "-framework MetalKit"
)
