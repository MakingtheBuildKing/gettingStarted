cmake_minimum_required(VERSION 2.8.3)
set(PROJECT_NAME Study)
project(${PROJECT_NAME})
set(CMAKE_VERBOSE_MAKEFILE no)
set(CMAKE_BUILD_TYPE Debug)
IF (WIN32)
  set(CMAKE_CXX_FLAGS "-g -std=c++11" )
  set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "./")
ELSE()
  set(CMAKE_CXX_FLAGS "-g -DNDEBUG -std=c++11")
  set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "./build")
ENDIF()
SET(PLATFORM_SPECIFIC_LIBS "-lpthread")

include_directories(
  ./
  include/
)

add_executable(${PROJECT_NAME}
  src/main.cpp
)

target_link_libraries(${PROJECT_NAME}
)
