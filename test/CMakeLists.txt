# Add the test executable
add_executable(MyLibraryTest MyLibraryTest.cpp)

# Link the test executable to the library and Google Test
target_link_libraries(MyLibraryTest PRIVATE MyLibrary gtest gtest_main)

# Specify the include directories for the test
target_include_directories(MyLibraryTest PRIVATE ${CMAKE_SOURCE_DIR}/src)

# Enable CTest support
enable_testing()

# Register the test with CTest
add_test(NAME MyLibraryTest COMMAND MyLibraryTest)

# Use GoogleTest's built-in test discovery
include(GoogleTest)
gtest_discover_tests(MyLibraryTest)