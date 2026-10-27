cmake_minimum_required(VERSION 2.8.4)

set(LIBHELLO_SRC hello.c)

add_library(hello_dynamic SHARED ${LIBHELLO_SRC})
add_library(hello_static STATIC ${LIBHELLO_SRC})

set_target_properties(hello_dynamic PROPERTIES
        OUTPUT_NAME "hello"
        VERSION 1.2
        SOVERSION 1
        LIBRARY_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}/lib")

set_target_properties(hello_static PROPERTIES
        OUTPUT_NAME "hello"
        ARCHIVE_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}/lib")

install(TARGETS hello_dynamic hello_static
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)
        
install(FILES hello.h DESTINATION include/hello)
