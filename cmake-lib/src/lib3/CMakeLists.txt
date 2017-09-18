add_library(cmake_lib3 SHARED lib3.h lib3.cpp)

target_include_directories(cmake_lib3 INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        )

install(TARGETS cmake_lib3 EXPORT cmakeLib DESTINATION lib INCLUDES DESTINATION include)
install(FILES lib3.h DESTINATION include )
