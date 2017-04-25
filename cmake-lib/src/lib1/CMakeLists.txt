set(SOURCE_FILES lib1.cpp lib1.h)

target_sources(cmake_lib PRIVATE lib1/lib1.h lib1/lib1.cpp)
target_include_directories(cmake_lib INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        $<INSTALL_INTERFACE:include>  # <prefix>/include/mylib
        )

install(FILES lib1.h DESTINATION include )
