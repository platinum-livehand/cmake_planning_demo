project(process)

# 生成动态库
add_library(${PROJECT_NAME}
SHARED
process.cpp
)

# 添加包含
target_include_directories(${PROJECT_NAME}
PUBLIC
${PNC_MAP_DIR}
)

# 链接库
target_link_libraries(${PROJECT_NAME}
PUBLIC
pnc_map
Eigen3::Eigen
)