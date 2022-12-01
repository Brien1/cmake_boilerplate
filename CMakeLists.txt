cmake_minimum_required(VERSION 3.14)
project(my_project)
# GoogleTest requires at least C++14
set(CMAKE_CXX_STANDARD 14)


enable_testing()
add_subdirectory(src)
add_subdirectory(tests)

add_executable(
  hello_test
  tests/hello_test.cpp 
)
add_executable(
main
src/main.cpp
)
    
target_link_libraries(srclib testslib)
target_link_libraries(hello_test Catch2::Catch2)
target_link_libraries(hello_test srclib)
target_link_libraries(main srclib)
