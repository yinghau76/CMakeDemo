add_library(hello src/hello.cpp) # target is a library

target_include_directories(hello
  PRIVATE res     # private include directories
  PUBLIC include  # public include directories
)

target_compile_definitions(hello
  PRIVATE INTERNAL_USE_HELLO
  INTERFACE EXTERNAL_USE_HELLO
)

target_compile_options(hello
  PRIVATE -v
  INTERFACE -w
)