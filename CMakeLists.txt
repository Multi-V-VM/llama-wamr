cmake_minimum_required(VERSION 3.22)
project(llama_wamr LANGUAGES C CXX)
set(CMAKE_CXX_STANDARD 20)
include_directories(wamr-ggml-llama)
add_executable(llama_wamr ${SOURCE_FILES} wamr-ggml-llama/llama.cpp ${UNCOMMON_SHARED_SOURCE})

target_link_libraries(llama_wamr -lm -ldl -lpthread)
