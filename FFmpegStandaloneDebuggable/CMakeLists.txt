cmake_minimum_required(VERSION 3.11)
project(FFmpegStandalone2)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_VERBOSE_MAKEFILE ON)

add_custom_command(OUTPUT ffmpeg_g
                    COMMAND make -j4
                    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/ffmpeg-4.0.1)

add_custom_target(ffmpeg
                    COMMAND make -j4
                    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/ffmpeg-4.0.1)