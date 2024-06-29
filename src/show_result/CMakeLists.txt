project(show_result)

# 生成动态库
add_library(${PROJECT_NAME}
SHARED
show_result.cpp
)

# 添加包含
target_include_directories(${PROJECT_NAME}
PUBLIC
${PROCESS_DIR}
${EASYX_DIR}/include
)

# 链接库
target_link_libraries(${PROJECT_NAME}
PUBLIC
process
${EASYX_DIR}/lib64/libeasyx.a
)