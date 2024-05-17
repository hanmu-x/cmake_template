
project(myLib)

# 搜索当前目录下的所有源文件
aux_source_directory(./ SRC)


add_library(${PROJECT_NAME} STATIC ${SRC})

# 设置库的生成的路径
set(LIBRARY_OUTPUT_PATH ${LIB_PATH})






