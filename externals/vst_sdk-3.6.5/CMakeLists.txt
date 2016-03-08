add_subdirectory(pluginterfaces)
add_subdirectory(base)
add_subdirectory(vstgui4)
add_subdirectory(public.sdk)

set(VST_INCLUDE ${CMAKE_CURRENT_SOURCE_DIR} CACHE INTERNAL "VST SDK includes" FORCE)
set(VST_LIBS "vst_intf;vst_base;vst;vst2;vsthosting;vstmain" CACHE INTERNAL "VST SDK libs" FORCE)
set(VST_GUI_LIB "vstgui" CACHE INTERNAL "VSG GUI lib" FORCE)
set(VST_GUI_INCLUDE "${CMAKE_CURRENT_SOURCE_DIR}/vstgui4" CACHE INTERNAL "VST GUI includes" FORCE)
