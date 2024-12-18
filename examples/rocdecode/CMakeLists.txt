cmake_minimum_required(VERSION 3.18.4 FATAL_ERROR)

project(rocprofiler-systems-rocdecode LANGUAGES CXX)

if(ROCPROFSYS_DISABLE_EXAMPLES)
    get_filename_component(_DIR ${CMAKE_CURRENT_LIST_DIR} NAME)

    if(${PROJECT_NAME} IN_LIST ROCPROFSYS_DISABLE_EXAMPLES OR ${_DIR} IN_LIST
                                                              ROCPROFSYS_DISABLE_EXAMPLES)
        return()
    endif()
endif()

add_subdirectory(videodecode)
