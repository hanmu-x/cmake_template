

project(myDll)

# 搜索当前目录下的所有源文件
aux_source_directory(./ SRC)

# 设置库的生成的路径
set(LIBRARY_OUTPUT_PATH ${LIB_PATH})

add_library(${PROJECT_NAME} SHARED ${SRC})







