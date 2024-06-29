project(planning_main)

add_subdirectory(pnc_map)
add_subdirectory(process)
add_subdirectory(show_result)

# 生成可执行程序
add_executable(${PROJECT_NAME} planning_main.cpp)

target_include_directories(${PROJECT_NAME}
PUBLIC
# 添加 process 库的包含
${PROCESS_DIR}
# 添加 show_result 库的包含
${SHOW_RESULT_DIR}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
# 链接 process 库
process
# 链接 show_result 库
show_result
)
