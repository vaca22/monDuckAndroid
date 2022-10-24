
cmake_minimum_required(VERSION 3.18.1)


project("monduckandroid")


add_subdirectory(lib/cJSON)
include_directories(lib/cJSON)

add_library(
        monduckandroid

        SHARED



        native-lib.cpp)



find_library(
        log-lib
        log)



target_link_libraries(
        monduckandroid
        cjson
        ${log-lib})