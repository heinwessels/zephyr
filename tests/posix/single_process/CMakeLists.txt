# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(posix_single_process)

FILE(GLOB app_sources src/*.c)

target_sources(app PRIVATE ${app_sources})

# For setenv() and unsetenv()
target_compile_options(app PRIVATE -U_POSIX_C_SOURCE -D_POSIX_C_SOURCE=200809L)
# For getenv_r() visibility and testing
target_compile_definitions(app PRIVATE _BSD_SOURCE)
