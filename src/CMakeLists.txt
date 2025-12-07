# Build Library
add_library(RDTSC STATIC ${CMAKE_SOURCE_DIR}/src/rdtsc/rdtsc.cpp)
target_include_directories(RDTSC PUBLIC ${CMAKE_SOURCE_DIR}/include)
# Build EXE
add_executable(RDTSC-EXE main.cpp)
target_link_libraries(RDTSC-EXE PRIVATE RDTSC)