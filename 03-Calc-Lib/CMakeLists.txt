# 源码在同目录下的cmake示例

cmake_minimum_required(VERSION 3.0)
project(Calc)

# 查找当前目录下的所有源文件，将名称存储到C_SRC变量
aux_source_directory(. C_SRC)

# 添加子目录
add_subdirectory(calc)

# 添加头文件路径
include_directories(calc)

#指定生成目标
add_executable(Calc ${C_SRC})

# 添加链接库
target_link_libraries(Calc CalcLib)