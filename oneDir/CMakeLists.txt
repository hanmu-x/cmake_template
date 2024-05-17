cmake_minimum_required(VERSION 3.15)

project(ondDir CXX)


# 检测系统版本
if (CMAKE_HOST_SYSTEM_NAME MATCHES "Windows")
    set(IS_WINDOWS TRUE)
    set(PLATFORM_NAME "Windows")
    message(STATUS "Target is Windows")

elseif (CMAKE_HOST_SYSTEM_NAME MATCHES "Linux")
    set(IS_LINUX TRUE)
    set(PLATFORM_NAME "Linux")
    message(STATUS "Target is Linux")

endif ()


# 检查系统位数
if (CMAKE_SIZEOF_VOID_P EQUAL 8)
    set(ARCH_NAME "x64")
    message(STATUS "Target is 64 bits")
else ()
    set(ARCH_NAME "x32")
    message(STATUS "Target is 32 bits")
endif ()

# 设置程序输出目录
# ${CMAKE_BUILD_TYPE}，表示根据构建类型（如 Debug 或 Release）
set(EXECUTABLE_OUTPUT_PATH "${CMAKE_SOURCE_DIR}/Bin/${PLATFORM_NAME}/${ARCH_NAME}/${CMAKE_BUILD_TYPE}")

add_executable(${PROJECT_NAME} main.cpp tool.cpp)



