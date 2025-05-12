#设置cmake版本
cmake_minimum_required(VERSION 3.31)

#项目名字
project(MiraclCoreCppBendmarking)

#设置编译版本
set(CMAKE_CXX_STANDARD 20)

#声明头文件路径
set(INC_DIR ${CMAKE_SOURCE_DIR}/include)
#声明链接库路径
set(LINK_DIR ${CMAKE_SOURCE_DIR}/lib)

#编译文件
add_executable(MiraclCoreCppBendmarking main.cpp)

# 添加头文件搜索路径
target_include_directories(MiraclCoreCppBendmarking PRIVATE ${INC_DIR})
# 添加库文件搜索路径
target_link_directories(MiraclCoreCppBendmarking PRIVATE ${LINK_DIR})

# 链接库
target_link_libraries(MiraclCoreCppBendmarking PRIVATE lib_miraclcore_bls12381_cpp_64.a)