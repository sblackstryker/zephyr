#
# Copyright (c) 2022 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: Apache-2.0
#

cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(fs_mgmt_hash_supported)

FILE(GLOB app_sources
	src/*.c
)

target_sources(app PRIVATE ${app_sources})
zephyr_library_include_directories(${ZEPHYR_BASE}/subsys/mgmt/mcumgr/)
