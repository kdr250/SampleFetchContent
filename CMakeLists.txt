cmake_minimum_required (VERSION 3.8)

project(SampleFetchContent VERSION 1.0 LANGUAGES CXX)

add_library(
	SampleFetchContent
	src/Vec2.h
	src/Vec2.cpp
)

set_target_properties(
  SampleFetchContent PROPERTIES
    C_VISIBILITY_PRESET hidden)

target_compile_definitions(
  SampleFetchContent PRIVATE FT2_BUILD_LIBRARY)

if (WIN32)
  target_compile_definitions(
    SampleFetchContent PRIVATE _CRT_SECURE_NO_WARNINGS _CRT_NONSTDC_NO_WARNINGS)
  if (BUILD_SHARED_LIBS)
    target_compile_definitions(
      SampleFetchContent PRIVATE DLL_EXPORT)
  endif ()
endif ()