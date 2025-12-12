#file(GLOB SLAC_SRCS *.c)
#foreach(src ${SLAC_SRCS})
#    get_filename_component(bin ${src} NAME_WE)
#    add_executable(${bin} ${src})
#    target_include_directories(${bin} PRIVATE ${CMAKE_SOURCE_DIR}/tools)
#    install(TARGETS ${bin} DESTINATION bin)
#endforeach()

# creating temporary object library to hold common sources
add_library(evse_cm_atten_char.o evse_cm_atten_char.c channel.h error.h memory.h slac.h)
add_library(evse_cm_atten_profile.o evse_cm_atten_profile.c channel.h error.h memory.h slac.h types.h)
add_library(evse_cm_mnbc_sound.o evse_cm_mnbc_sound.c channel.h error.h memory.h slac.h) 
add_library(evse_cm_slac_match.o evse_cm_slac_match.c channel.h error.h memory.h slac.h types.h)
add_library(evse_cm_slac_param.o evse_cm_slac_param.c channel.h error.h memory.h slac.h types.h)
add_library(evse_cm_start_atten_char.o evse_cm_start_atten_char.c channel.h error.h memory.h slac.h)
add_library(pev_cm_atten_char.o pev_cm_atten_char.c channel.h error.h memory.h slac.h)
add_library(pev_cm_mnbc_sound.o pev_cm_mnbc_sound.c channel.h error.h memory.h slac.h types.h)
add_library(pev_cm_slac_match.o pev_cm_slac_match.c channel.h error.h memory.h slac.h types.h)
add_library(pev_cm_slac_param.o pev_cm_slac_param.c channel.h error.h memory.h slac.h types.h)
add_library(pev_cm_start_atten_char.o pev_cm_start_atten_char.c channel.h error.h slac.h types.h)
add_library(slac_session.o slac_session.c memory.h slac.h)
add_library(slac_structs.o slac_structs.c slac.h)


