add_library(testslib hello_test.cpp)
include(FetchContent)

  
FetchContent_Declare(
    Catch2
    GIT_REPOSITORY https://github.com/catchorg/Catch2.git
    GIT_TAG        v2.13.1)
  
FetchContent_MakeAvailable(Catch2)
target_link_libraries(testslib PUBLIC Catch2::Catch2) 
