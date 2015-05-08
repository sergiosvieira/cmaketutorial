file(GLOB SOURCES "*.cpp")
set(PUBLIC_SOURCES ${SOURCES} PARENT_SCOPE)
add_subdirectory(submodule)
add_library(header ${SOURCES} ${PUBLIC_HEADERS})