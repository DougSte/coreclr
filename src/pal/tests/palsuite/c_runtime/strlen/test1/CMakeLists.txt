cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test1.c
)

add_executable(paltest_strlen_test1
  ${SOURCES}
)

add_dependencies(paltest_strlen_test1 CoreClrPal)

target_link_libraries(paltest_strlen_test1
  pthread
  m
  CoreClrPal
)
