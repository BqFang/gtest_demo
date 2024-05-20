cmake_minimum_required(VERSION 3.0)

project(GTEST_WIN)

# 头文件目录
include_directories("${CMAKE_CURRENT_SOURCE_DIR}/src/calculate/include")

# 源文件目录
# AUX_SOURCE_DIRECTORY 找到目录下的所有源文件，存在变量 DIR_SRCS 中，变量的引用 ${DIR_SRCS}
AUX_SOURCE_DIRECTORY("${CMAKE_CURRENT_SOURCE_DIR}/src/calculate" DIR_SRCS)

add_executable(calculate ./src/main.c ${DIR_SRCS})

