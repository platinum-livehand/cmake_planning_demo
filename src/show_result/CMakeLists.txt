project(show_result)

add_library(${PROJECT_NAME}
SHARED
show_result.cpp
)

# Ìí¼Ó process ¿â
target_include_directories(${PROJECT_NAME}
PUBLIC
${PROCESS_DIR}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)

# Ìí¼Ó EasyX ¿â
target_include_directories(${PROJECT_NAME}
PUBLIC
${EasyX_DIR}/include
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
${EasyX_DIR}/lib64/libeasyx.a
)