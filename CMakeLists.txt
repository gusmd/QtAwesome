cmake_minimum_required(VERSION 3.2)

project(QtAwesome)

add_library(QtAwesome STATIC
    QtAwesome/QtAwesome.cpp
    QtAwesome/QtAwesome.h
    QtAwesome/QtAwesome.qrc
    QtAwesome/QtAwesomeAnim.cpp
    QtAwesome/QtAwesomeAnim.h
)

set_target_properties(QtAwesome
    PROPERTIES
    CXX_STANDARD 14
    CXX_EXTENSIONS OFF
    AUTOMOC ON
    AUTORCC ON
)

target_include_directories(QtAwesome PUBLIC
    QtAwesome
)

find_package(Qt5Widgets)
target_link_libraries(QtAwesome
    PUBLIC Qt5::Widgets
)
