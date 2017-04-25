set(SOURCE_FILES lib2.cpp lib2.h)

target_sources(cmake_lib PRIVATE lib2/lib2.h lib2/lib2.cpp)
target_include_directories(cmake_lib INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        $<INSTALL_INTERFACE:include>  # <prefix>/include/mylib
        )

install(FILES lib2.h DESTINATION include )
