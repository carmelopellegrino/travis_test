cmake_minimum_required (VERSION 2.6)
project (sqrt2)

find_package(Boost 1.53 REQUIRED COMPONENTS atomic system thread program_options chrono)

# Compiler flags
set(GCC_COMPILE_FLAGS "")

# Linker flags
set(GCC_LINK_FLAGS "-m")

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GCC_COMPILE_FLAGS} ${GCC_LINK_FLAGS}")

# Install prefix
set(CMAKE_INSTALL_PREFIX "${PROJECT_SOURCE_DIR}/arch")

add_executable(sqrt2 main.c)

# Intall
install(TARGETS sqrt2 DESTINATION bin)
