# Add the library's source files
add_library(MyLibrary STATIC
    MyLibrary.cpp
)

# Specify include directories for the library
target_include_directories(MyLibrary PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})