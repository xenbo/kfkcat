cmake_minimum_required(VERSION 3.13)
project(kfkcat)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(yajl)
include_directories(yajl/api)

add_executable(kfkcat kafkacat.c  format.c tools.c)
#        json.c yajl/yajl.c yajl/yajl_lex.c yajl/yajl_parser.c yajl/yajl_buf.c yajl/yajl_encode.c yajl/yajl_gen.c yajl/yajl_alloc.c yajl/yajl_tree.c yajl/yajl_version.c)
target_link_libraries(kfkcat rdkafka)