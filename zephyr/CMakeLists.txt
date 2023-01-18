if(CONFIG_LIBSAMPLE)
  add_subdirectory(.. build)
  set_property(GLOBAL APPEND PROPERTY ZEPHYR_INTERFACE_LIBS sample)
  # this is for importing header only libraries
  # zephyr_include_directories(
  #   ..
  # )
  # zephyr_interface_library_named(sample)
endif()
