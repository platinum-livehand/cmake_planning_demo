project(planning_main)

add_subdirectory(pnc_map)
add_subdirectory(process)
add_subdirectory(show_result)

# 生成可执行程序
add_executable(${PROJECT_NAME} planning_main.cpp)

# 添加包含
target_include_directories(${PROJECT_NAME}
PUBLIC
${PROCESS_DIR}
${SHOW_RESULT_DIR}
)

# 链接库
target_link_libraries(${PROJECT_NAME}
PUBLIC
process
show_result
)
