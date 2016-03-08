project(vstgui)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/vstgui)

set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/vstgui)

set(SRC
    #${SRC_DIR}/vstgui_win32.cpp
    ${SRC_DIR}/vstgui_uidescription_win32.cpp
    ${SRC_DIR}/vstgui.cpp
)

# Supress unsafe functions warning
add_definitions(/wd4996)

add_library(${PROJECT_NAME} ${SRC})
