add_library(mylib x.c)

target_include_directories(mylib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
