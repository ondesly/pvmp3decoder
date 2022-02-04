#
#  CMakeLists.txt
#  pvmp3decoder
#
#  Created by Dmitrii Torkhov <dmitriitorkhov@gmail.com> on 04.02.2022.
#  Copyright © 2022 Dmitrii Torkhov. All rights reserved.
#

cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(pvmp3decoder
        VERSION 1.0.1
        LANGUAGES C CXX)

#########
# Build #
#########

add_subdirectory(src)