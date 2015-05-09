file(GLOB HEADERS "*.h")
set(PUBLIC_HEADERS ${HEADERS} PARENT_SCOPE)
add_subdirectory(submodule)