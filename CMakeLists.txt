cmake_minimum_required(VERSION 3.17)
project(clean-test-win)

set(CMAKE_CXX_STANDARD 20)

include(FetchContent)
fetchcontent_declare(
  CleanTest
  GIT_REPOSITORY https://github.com/clean-test/clean-test.git
  GIT_TAG        main # or a fixed tag e.g. v1.2.0
)
fetchcontent_makeavailable(CleanTest)

add_executable(clean-test-win test.cpp)
target_link_libraries(clean-test-win CleanTest::main-static)
