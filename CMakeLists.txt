cmake_minimum_required(VERSION 3.10)
project(open-plc-utils C)

# Set C standard
set(CMAKE_C_STANDARD 99)

# Add global include directories
include_directories(${CMAKE_SOURCE_DIR}/tools)

# Add subdirectories
add_subdirectory(ether)
add_subdirectory(key)
add_subdirectory(mdio)
add_subdirectory(mme)
add_subdirectory(nvm)
add_subdirectory(nodes)
add_subdirectory(pib)
add_subdirectory(plc)
add_subdirectory(ram)
add_subdirectory(serial)
add_subdirectory(slac)
add_subdirectory(tools)
