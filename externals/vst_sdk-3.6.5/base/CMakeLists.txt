project(vst_base)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/source)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/source/*.cpp)
file(GLOB HDRS ${CMAKE_CURRENT_SOURCE_DIR}/source/*.h)

add_library(${PROJECT_NAME} ${SRC} ${HDRS})
target_link_libraries(${PROJECT_NAME} vst_intf)