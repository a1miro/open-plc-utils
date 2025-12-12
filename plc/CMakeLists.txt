# CMake build file for plc directory
file(GLOB PLC_SRCS *.c)

# List of all executables to build (from Makefile TOOLS variable)
set(PLC_TOOLS
    int6k int6kboot int6keth int6kf int6khost int64host int6kid int6klist int6klog int6kmdio int6kmdio2 int6kmod int6kstat int6ktest int6krate int6krule int6ktone int6kwait CMEncrypt sada coqos_add coqos_info coqos_man coqos_mod coqos_rel mdustats
    ampboot amphost ampID amplist amprate amprule ampstat amptest amptool amptone ampwait
    plcboot plchost plcID plclist plcrate plcrule plcstat plctest plctool plctone plcwait plchostd plchostd2 plcget plcset plcotst plcfwd plcdevs plclog plcmdio16 plcmdio32
)

# For each tool, add executable if the source exists
foreach(tool ${PLC_TOOLS})
    if(EXISTS ${CMAKE_CURRENT_SOURCE_DIR}/${tool}.c)
        add_executable(${tool} ${tool}.c)
        target_link_libraries(${tool} PRIVATE m)
        target_include_directories(${tool} PRIVATE ${CMAKE_SOURCE_DIR}/tools)
        install(TARGETS ${tool} DESTINATION bin)
    endif()
endforeach()
