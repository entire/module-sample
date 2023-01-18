project(sample)
cmake_minimum_required(VERSION 3.20)

add_library(sample)
target_compile_options(sample PRIVATE -Wall -Wextra)
set_target_properties(sample PROPERTIES C_STANDARD 11)

target_include_directories(sample PUBLIC 
  # sample1
  # sample2
  .
)
target_sources(sample PRIVATE
  sample1/src/plain.c
)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
