#
#  CMakeLists.txt
#  pvmp3decoder
#
#  Created by Dmitrii Torkhov <dmitriitorkhov@gmail.com> on 04.02.2022.
#  Copyright © 2022 Dmitrii Torkhov. All rights reserved.
#

set(SRC
        pvmp3/pvmp3_normalize.cpp
        pvmp3/pvmp3_alias_reduction.cpp
        pvmp3/pvmp3_crc.cpp
        pvmp3/pvmp3_decode_header.cpp
        pvmp3/pvmp3_decode_huff_cw.cpp
        pvmp3/pvmp3_getbits.cpp
        pvmp3/pvmp3_dequantize_sample.cpp
        pvmp3/pvmp3_framedecoder.cpp
        pvmp3/pvmp3_get_main_data_size.cpp
        pvmp3/pvmp3_get_side_info.cpp
        pvmp3/pvmp3_get_scale_factors.cpp
        pvmp3/pvmp3_mpeg2_get_scale_data.cpp
        pvmp3/pvmp3_mpeg2_get_scale_factors.cpp
        pvmp3/pvmp3_mpeg2_stereo_proc.cpp
        pvmp3/pvmp3_huffman_decoding.cpp
        pvmp3/pvmp3_huffman_parsing.cpp
        pvmp3/pvmp3_tables.cpp
        pvmp3/pvmp3_imdct_synth.cpp
        pvmp3/pvmp3_mdct_6.cpp
        pvmp3/pvmp3_dct_6.cpp
        pvmp3/pvmp3_poly_phase_synthesis.cpp
        pvmp3/pvmp3_equalizer.cpp
        pvmp3/pvmp3_seek_synch.cpp
        pvmp3/pvmp3_stereo_proc.cpp
        pvmp3/pvmp3_reorder.cpp
        pvmp3/pvmp3_polyphase_filter_window.cpp
        pvmp3/pvmp3_mdct_18.cpp
        pvmp3/pvmp3_dct_9.cpp
        pvmp3/pvmp3_dct_16.cpp)

add_library(pvmp3decoder STATIC ${SRC})

#

target_include_directories(pvmp3decoder
        PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/../include>
        PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/../include/pvmp3>
        PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/pvmp3>)

set_target_properties(pvmp3decoder PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED YES CXX_EXTENSIONS NO)