cmake_minimum_required(VERSION 3.10)
project(vf2lib)

#set(CMAKE_CXX_STANDARD 20)
#set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)


# Create the library with the source files
add_library(vf2lib STATIC
"src/argedit.cc"
"src/argloader.cc"
"src/argraph.cc"
"src/error.cc"
"src/gene_mesh.cc"
"src/gene.cc"
"src/match.cc"
"src/sd_state.cc"
"src/sortnodes.cc"
"src/ull_state.cc"
"src/ull_sub_state.cc"
"src/vf_mono_state.cc"
"src/vf_sub_state.cc"
"src/vf2_mono_state.cc"
"src/vf2_state.cc"
"src/vf2_sub_state.cc"
"src/xsubgraph.cc"
)

# Include the directory with the headers
target_include_directories(vf2lib PUBLIC include)
target_compile_options(vf2lib PRIVATE -Wno-write-strings -Wno-deprecated)


# Link necessary libraries
target_link_libraries(vf2lib PUBLIC pthread atomic)