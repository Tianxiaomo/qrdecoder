# cmake_minimum_required(VERSION 2.8)
# project(demo)
# 
# add_definitions("-Wall -g -Wno-unknown-warning-option"
#         " -Wno-format-extra-args -Wno-format -Wno-pragmas"
#         " -Wno-incompatible-pointer-types")

# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目信息
project (demo)

# 指定生成目标
# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(./src DIR_SRCS)
aux_source_directory(./src/zxing DIR_SRCS)

# 生成链接库
add_library (demo ${DIR_SRCS})