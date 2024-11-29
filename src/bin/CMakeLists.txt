add_executable(myapp main.c)

target_link_libraries(myapp PRIVATE mylib)

# target_include_directories(myapp PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
