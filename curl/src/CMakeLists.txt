add_executable(curltest main.c)

find_package(CURL REQUIRED)
target_link_libraries(curltest PRIVATE CURL::libcurl)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
