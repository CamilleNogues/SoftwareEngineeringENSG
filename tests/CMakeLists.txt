cmake_minimum_required(VERSION 3.10)

if(NOT TARGET basic)
# set the project name
project(HelloProjTests)
find_package(HelloProj)
enable_testing()
endif()

# set the project name
#(HelloProjTests VERSION 1.0)
#find_package(HelloProj)
#enable_testing()

add_executable(test_hello test_hello.cpp)
target_link_libraries(test_hello PUBLIC basic)
add_test(NAME test_hello COMMAND test_hello)

add_executable(test_version test_version.cpp)
target_link_libraries(test_version PUBLIC basic)
add_test(NAME test_version COMMAND test_version)