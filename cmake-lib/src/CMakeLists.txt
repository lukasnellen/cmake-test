add_library(cmake_lib SHARED)

add_subdirectory(lib1)
add_subdirectory(lib2)
add_subdirectory(lib3)

install(TARGETS cmake_lib EXPORT cmakeLib DESTINATION lib INCLUDES DESTINATION include)
install(EXPORT cmakeLib DESTINATION share/cmake/cmakeLib FILE cmakeLibConfig.cmake)
