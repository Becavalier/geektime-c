cmake_minimum_required(VERSION 3.10)
# 设置项目名称；
project(Test)
# 设置二进制目标文件名称；
set(TARGET_FILE "main")
# 添加源文件目录；
aux_source_directory(./src DIR_SRCS)
# 设置二进制目标文件的依赖；
add_executable(${TARGET_FILE} ${DIR_SRCS})
# 设置头文件查找目录；
target_include_directories(${TARGET_FILE} PUBLIC "${PROJECT_SOURCE_DIR}/include")
# 设置需要链接的库；
target_link_libraries(${TARGET_FILE} PUBLIC m)
