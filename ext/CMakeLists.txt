cmake_minimum_required (VERSION 2.8)
project (VoxRes)

include_directories($ENV{SC_PATH}/include/plugin_interface)
include_directories($ENV{SC_PATH}/include/common)
include_directories($ENV{SC_PATH}/external_libraries/libsndfile/)

set(CMAKE_SHARED_MODULE_PREFIX "")
if(APPLE OR WIN32)
	set(CMAKE_SHARED_MODULE_SUFFIX ".scx")
endif()

add_library(VoxRes MODULE VoxRes.cpp)
find_library(VOX_BOX_LIBRARIES NAMES vox_box_supercollider
	libvox_box_supercollider PATHS ../target/release)
target_link_libraries(VoxRes PRIVATE ${VOX_BOX_LIBRARIES})
install(TARGETS VoxRes DESTINATION .)
