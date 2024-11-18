cmake_minimum_required(VERSION 3.10)
project(vf2lib)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

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

target_include_directories(vf2lib PUBLIC include)