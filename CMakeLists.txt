cmake_minimum_required (VERSION 2.6)
project (tianlongbabu)


SET(BOOST_INCLUDE_DIR /usr/local/Cellar/boost/1.62.0/include)
SET(BOOST_LIBRARY_DIR /usr/local/Cellar/boost/1.62.0/lib)

FIND_PACKAGE(Boost COMPONENTS system filesystem REQUIRED)

#include the headers
include_directories(include)
include_directories(${BOOST_INCLUDE_DIR})

file(GLOB SOURCES "src/*.cpp")

add_executable(experiment ${SOURCES})
