project(map_test)

add_executable(${PROJECT_NAME} map_test.cpp)

target_include_directories(${PROJECT_NAME}
PUBLIC
${PNC_MAP_DIR}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
pnc_map
)

add_test(
    NAME ${PROJECT_NAME}
    COMMAND ${PROJECT_NAME}
)