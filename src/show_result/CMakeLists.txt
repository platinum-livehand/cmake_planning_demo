project(show_result)

add_library(${PROJECT_NAME}
SHARED
show_result.cpp
)

# 添加 process 库
target_include_directories(${PROJECT_NAME}
PUBLIC
${PROCESS_DIR}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)

# 添加 EasyX 库的包含
target_include_directories(${PROJECT_NAME}
PUBLIC
${EASYX_DIR}/include
)

# 链接 EasyX 库
target_link_libraries(${PROJECT_NAME}
PUBLIC
${EASYX_DIR}/lib64/libeasyx.a
)