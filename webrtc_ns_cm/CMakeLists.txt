
cmake_minimum_required(VERSION 3.15)
project(webrtc_ns_cm)

set(CMAKE_CXX_STANDARD 14)

include(./.SET_LOCAL_PATH.cmake)

if(MSVC)
    SET(CMAKE_CXX_FLAGS "/utf-8" "${CMAKE_CXX_FLAGS}")    # for CPP
    SET(CMAKE_C_FLAGS "/utf-8" "${CMAKE_C_FLAGS}")        # for C
endif(MSVC)

aux_source_directory(./include CPPLIST)

add_executable(
        ${PROJECT_NAME}
        ${CPPLIST}
        webrtc_ns_cm.cpp
        )




target_include_directories( ${PROJECT_NAME}
        PRIVATE
        ${PROJECT_SOURCE_DIR}/include

        )
        
