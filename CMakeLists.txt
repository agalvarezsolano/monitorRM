cmake_minimum_required(VERSION 3.9)
project(monitorRM)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_PREFIX_PATH "/home/adrian/Qt/5.5/gcc")
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
find_package(Qt5Core REQUIRED)
find_package(Qt5Widgets REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Network REQUIRED)
find_package(Qt5Sql REQUIRED)
find_package(Qt5Xml REQUIRED)
find_package(Qt5PrintSupport REQUIRED)





set(SOURCE_FILES
        main.cpp
        mainwindow.cpp
        mainwindow.h
        mainwindow.ui
        monitorRM.pro
        monitorRM.pro.user)

add_executable(monitorRM ${SOURCE_FILES})
target_link_libraries(monitorRM Qt5::Widgets Qt5::Core Qt5::Network Qt5::Sql ${Boost_LIBRARIES})