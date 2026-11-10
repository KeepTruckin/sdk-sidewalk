#
# Copyright (c) 2022 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause
#

set(SID_LIB_DIR ${ZEPHYR_BASE}/../sidewalk/lib/cortex-m4/ble_only)

# In SDK 2.0.0 libsidewalk_sdk.a and libace_ama.a reference each other, and
# libace_ama.a needs nanopb. GNU ld resolves archives in order, so group them.
zephyr_library_link_libraries(
  -Wl,--start-group
  ${SID_LIB_DIR}/libsidewalk_sdk.a
  ${SID_LIB_DIR}/libace_ama.a
  ${SID_LIB_DIR}/libext_nanopb.a
  -Wl,--end-group
)
