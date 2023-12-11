cmake_minimum_required (VERSION 3.8)

project(SampleFetchContent VERSION 1.0 LANGUAGES CXX)

add_library(SampleFetchContent SHARED src/Vec2.hpp src/Vec2.cpp)
