add_subdirectory(say)

add_executable(demo demo.cpp)

target_link_libraries(demo say hello)
