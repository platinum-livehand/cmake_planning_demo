project(process)

# 生成动态库
add_library(${PROJECT_NAME}
SHARED
process.cpp
)

# 添加 pnc_map 库的包含
target_include_directories(${PROJECT_NAME}
PUBLIC
${PNC_MAP_DIR}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
# 添加 pnc_map 库
pnc_map
# 添加 Eigen 库
Eigen3::Eigen
)