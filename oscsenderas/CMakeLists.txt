cmake_minimum_required(VERSION 4.3.0)

project(QLABWIN VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets Svg)

qt_standard_project_setup()

qt_add_executable(QLABWIN qlabs.cpp)

target_link_libraries(QLABWIN PRIVATE
    Qt6::Widgets
    Qt6::Svg
)
set_target_properties(QLABWIN PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
)