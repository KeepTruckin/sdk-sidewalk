#
# Copyright (c) 2022 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause
#

set(SID_LIB_DIR ${ZEPHYR_BASE}/../sidewalk/lib/cortex-m4/ble_only)

zephyr_library_link_libraries(${SID_LIB_DIR}/libace_ama.a)
zephyr_library_link_libraries(${SID_LIB_DIR}/libext_nanopb.a)
zephyr_library_link_libraries(${SID_LIB_DIR}/libsidewalk_pal.a)
zephyr_library_link_libraries(${SID_LIB_DIR}/libsidewalk_sdk.a)
