project(sample)
cmake_minimum_required(VERSION 3.20)

add_library(sample)
target_compile_options(sample PRIVATE -Wall -Wextra)
set_target_properties(sample PROPERTIES C_STANDARD 11)

target_include_directories(sample PUBLIC 
  .
)
target_sources(sample PRIVATE
  sample1/src/plain.c
  sample2/sample2.c
)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
