# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)

list(APPEND BOARD_ROOT ${CMAKE_CURRENT_SOURCE_DIR})
set(BOARD bandy_nrf52840)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(hello_world)

# NORDIC SDK APP START
target_sources(app PRIVATE src/main.c src/blinky.c)

# NORDIC SDK APP END
