cmake_minimum_required(VERSION 3.15)

project(MyLibrary LANGUAGES CXX)

# Optionally, set the C++ standard here
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Enable testing
enable_testing()

# Add the library's source and headers
add_subdirectory(src)

# Add the test folder and setup Google Test
add_subdirectory(test)

# Fetch Google Test only for testing purposes
include(FetchContent)
FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG release-1.10.0  # You can specify a specific release or branch
)
FetchContent_MakeAvailable(googletest)

# Disable -Werror for Google Test to avoid treating warnings as errors
target_compile_options(gtest PRIVATE
    -Wno-error       # Disable treating warnings as errors
    -Wno-maybe-uninitialized  # Disable maybe-uninitialized warning
)