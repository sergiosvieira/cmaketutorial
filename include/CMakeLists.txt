file(GLOB HEADERS "*.h")
set(PUBLIC_HEADERS ${HEADERS} PARENT_SCOPE)
include_directories(submodule)
add_subdirectory(submodule)