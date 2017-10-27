# CMake 最低版本号要求
cmake_minimum_required(VERSION 2.8)

# 项目信息
project(main01)

# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)

add_subdirectory(hello)

include_directories(./hello)

# 指定生成目标
add_executable(main ${DIR_SRCS})

target_link_libraries(main HELLO_LD)
