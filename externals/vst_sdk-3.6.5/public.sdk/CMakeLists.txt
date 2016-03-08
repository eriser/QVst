project(vsk_public_sdk)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/source)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../vstgui4)

file(GLOB SRC_COMMON ${CMAKE_CURRENT_SOURCE_DIR}/source/common/*.cpp)
file(GLOB HDRS_COMMON ${CMAKE_CURRENT_SOURCE_DIR}/source/common/*.h)

file(GLOB SRC_HOSTING ${CMAKE_CURRENT_SOURCE_DIR}/source/vst/hosting/*.cpp)
file(GLOB HDRS_HOSTING ${CMAKE_CURRENT_SOURCE_DIR}/source/vst/hosting/*.h)

file(GLOB SRC_VST ${CMAKE_CURRENT_SOURCE_DIR}/source/vst/*.cpp)
file(GLOB HDRS_VST ${CMAKE_CURRENT_SOURCE_DIR}/source/vst/*.h)
#list(REMOVE_ITEM SRC_VST ${CMAKE_CURRENT_SOURCE_DIR}/source/vst/vsteditcontroller.cpp)

file(GLOB SRC_VST2 ${CMAKE_CURRENT_SOURCE_DIR}/source/vst2.x/*.cpp)
file(GLOB HDRS_VST2 ${CMAKE_CURRENT_SOURCE_DIR}/source/vst2.x/*.h)

file(GLOB SRC_MAIN ${CMAKE_CURRENT_SOURCE_DIR}/source/main/*.cpp)
file(GLOB HDRS_MAIN ${CMAKE_CURRENT_SOURCE_DIR}/source/main/*.h)


# Supress unsafe functions warning
add_definitions(/wd4996)

add_library(vst ${SRC_VST} ${SRC_COMMON} ${HRDS_VSR} ${HDRS_COMMON})
#target_link_libraries(vst vstgui)
add_library(vsthosting ${SRC_HOSTING} ${SRC_COMMON} ${HDRS_HOSTING} ${HDRS_COMMON})
add_library(vst2 ${SRC_VST2} ${SRC_COMMON} ${HDRS_VST2} ${HDRS_COMMON})
add_library(vstmain ${SRC_MAIN} ${HDRS_MAIN})
