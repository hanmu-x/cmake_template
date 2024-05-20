
project(test )

aux_source_directory(./ SRC)

include_directories(../tool_lib)
include_directories(../tool_dll)

# 链接静态库
link_libraries(myLib)

# 生成可执行文件
add_executable(${PROJECT_NAME} ${SRC})

target_link_libraries(${PROJECT_NAME} PUBLIC myDll)



