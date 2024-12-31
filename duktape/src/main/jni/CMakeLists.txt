cmake_minimum_required(VERSION 3.4.1)

file(GLOB_RECURSE duktape_SRC
    "*.h"
    "*.c"
    "*.cpp"
)

add_library(duktape SHARED ${duktape_SRC})

target_link_libraries(duktape)
target_link_options(duktape PRIVATE "-Wl,-z,max-page-size=16384")
