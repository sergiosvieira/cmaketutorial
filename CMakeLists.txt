cmake_minimum_required(VERSION 3.0)
project(tutorial CXX)
if ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "GNU" OR
    "${CMAKE_CXX_COMPILER_ID}" STREQUAL "Cland")
    set(warnings "-Wall -Wextra -std=c++11")
elseif ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "MSVC")
    set(warnings "/W4 /WX /EHsc")
endif()
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${warnings}")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${warnings}")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)

include_directories(include)
add_subdirectory(include)
add_subdirectory(src)
add_executable(siga 
			   main.cpp)
target_link_libraries(siga 
					  header)
message(STATUS "-->" ${PUBLIC_SOURCES})
