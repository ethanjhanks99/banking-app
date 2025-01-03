cmake_minimum_required(VERSION 3.12)

set(PROJECT Banking)

set(HEADER_FILES 
  tools.hpp
)
set(SOURCE_FILES 
  tools.cpp
)

project(${PROJECT})

add_executable(${PROJECT} ${HEADER_FILES} ${SOURCE_FILES} main.cpp)

set_property(TARGET ${PROJECT} PROPERTY CXX_STANDARD 23)

if (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
  target_compile_options(${PROJECT} PRIVATE /W4 /permissive-)
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
  target_compile_options(${PROJECT} PRIVATE -Wall -Wextra -pedantic)
elseif (CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  target_compile_options(${PROJECT} PRIVATE -Wall -Wextra -pedantic)
endif()

find_program(CLANG_FORMAT "clang-format")
if (CLANG_FORMAT)
    unset(SOURCE_FILES_PATHS)
    foreach(SOURCE_FILE ${HEADER_FILES} ${SOURCE_FILES} main.cpp)
        get_source_file_property(WHERE ${SOURCE_FILE} LOCATION)
        set(SOURCE_FILES_PATHS ${SOURCE_FILES_PATHS} ${WHERE})
    endforeach()

    add_custom_target(
        ClangFormat
        COMMAND ${CLANG_FORMAT}
        -i
        -style=file
        ${SOURCE_FILES_PATHS})

    add_dependencies(${PROJECT} ClangFormat)

endif()

# include(FetchContent)
# FetchContent_Declare(
#   googletest
#   GIT_REPOSITORY  https://github.com/google/googletest.git
#   GIT_TAG         v1.14.0
# )
# set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
# FetchContent_MakeAvailable(googleTest)

# target_link_libraries(${UNIT_TEST_RUNNER} gtest_main)