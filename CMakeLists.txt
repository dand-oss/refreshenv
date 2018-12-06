cmake_minimum_required(VERSION 2.8)
project(refreshenvs CXX)
set(exename "refreshenvs")

###############
# ASI default settings
list(APPEND CMAKE_MODULE_PATH "$ENV{ASV_CMAKE}")
include(asv_cmake_defaults)
asv_cmake_defaults( )
###############

set(refreshenvs_sources refreshenvs.cpp)
add_executable(refreshenvs ${refreshenvs_sources})

install(TARGETS ${exename} DESTINATION bin)
