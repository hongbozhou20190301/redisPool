CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12.2)

PROJECT(opcredisPool)

add_definitions("-g -Wall")

LINK_DIRECTORIES("/usr/local/lib")

LINK_LIBRARIES(pthread hiredis z dl rt  m)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

AUX_SOURCE_DIRECTORY(./ DIR_SRCS)

ADD_EXECUTABLE(opcredisPool  ${DIR_SRCS})
