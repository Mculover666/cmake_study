# 查找源文件
aux_source_directory(. C_SRCS)

# 生成链接库
add_library(CalcLib ${C_SRCS})
