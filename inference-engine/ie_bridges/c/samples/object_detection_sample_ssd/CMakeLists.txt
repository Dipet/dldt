# Copyright (C) 2018-2020 Intel Corporation
# SPDX-License-Identifier: Apache-2.0
#

set (TARGET_NAME "object_detection_sample_ssd_c")

# create sample target

add_executable(${TARGET_NAME} main.c)

target_link_libraries(${TARGET_NAME} PRIVATE ${InferenceEngine_LIBRARIES} opencv_c_wraper)

if(COMMAND add_cpplint_target)
    add_cpplint_target(${TARGET_NAME}_cpplint FOR_TARGETS ${TARGET_NAME})
endif()
