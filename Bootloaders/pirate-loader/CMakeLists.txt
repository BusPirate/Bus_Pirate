# This file is part of the Bus Pirate project
# (http://code.google.com/p/the-bus-pirate/).
#
# Written and maintained by the Bus Pirate project.
#
# To the extent possible under law, the project has
# waived all copyright and related or neighboring rights to Bus Pirate. This
# work is published from United States.
#
# For details see: http://creativecommons.org/publicdomain/zero/1.0/.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
project(pirate-loader)
set (SOURCE_FILES pirate-loader.c)
set_property (SOURCE ${SOURCE_FILES} PROPERTY COMPILE_DEFINITIONS OS=${CMAKE_SYSTEM_NAME})
set (CMAKE_EXE_LINKER_FLAGS "-static -static-libgcc")
add_executable (pirate-loader ${SOURCE_FILES})
