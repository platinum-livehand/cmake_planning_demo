cmake_minimum_required(VERSION 3.29.0)
project(planning
    VERSION 0.0.1
    DESCRIPTION "a demo of cmake planning"
    HOMEPAGE_URL "https://github.com/platinum-livehand/cmake_planning_demo"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# 目录变量
set(PROCESS_DIR ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_MAP_DIR ${CMAKE_SOURCE_DIR}/src/pnc_map)
set(SHOW_RESULT_DIR ${CMAKE_SOURCE_DIR}/src/show_result)
set(EASYX_DIR ${CMAKE_SOURCE_DIR}/third_party/EasyX)
set(EIGEN3_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/third_party/eigen-3.4.0)

list(APPEND CMAKE_MODULE_PATH "${EIGEN3_INCLUDE_DIR}/cmake")

message("CMAKE_MODULE_PATH = ${CMAKE_MODULE_PATH}")

find_package(Eigen3 3.4 REQUIRED)

# 添加子目录
add_subdirectory(src)