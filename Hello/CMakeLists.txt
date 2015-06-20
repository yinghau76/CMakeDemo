add_library(Hello src/hello.cpp) # target is a library

target_include_directories(Hello
  PRIVATE res     # private include directories
  PUBLIC include  # public include directories
)

target_compile_definitions(Hello
  PRIVATE INTERNAL_USE_HELLO
  INTERFACE EXTERNAL_USE_HELLO
)

target_compile_options(Hello
  PRIVATE -v
  INTERFACE -w
)