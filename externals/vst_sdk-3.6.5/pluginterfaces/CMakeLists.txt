project(vst_intf)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/base)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/base/*.cpp)
file(GLOB HDRS ${CMAKE_CURRENT_SOURCE_DIR}/base/*.h)

add_library(${PROJECT_NAME} ${SRC} ${HDRS})