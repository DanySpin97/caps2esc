# CMakeLists files in this project can
# refer to the root source directory of the project as ${HELLO_SOURCE_DIR} and
# to the root binary directory of the project as ${HELLO_BINARY_DIR}.
cmake_minimum_required (VERSION 2.8.11)
project (caps2esc)

set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -levdev -ludev")

include_directories("/usr/include/libevdev-1.0")

# Add executable called "helloDemo" that is built from the source files
# "demo.cxx" and "demo_b.cxx". The extensions are automatically found.
add_executable (caps2esc caps2esc.c)

install (
	TARGETS caps2esc
        RUNTIME DESTINATION bin
	)
