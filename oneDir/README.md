
该项目是一个单级目录的cmake构建的c++项目

如果要新加cpp文件,在编译时要在`CMakeLists.txt`文件中最后一行`add_executable(${PROJECT_NAME} main.cpp tool.cpp)` 这里将新加的cpp文件加上


