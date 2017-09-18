set(SOURCE_FILES lib2.cpp lib2.h)

target_sources(cmake_lib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/lib2.h ${CMAKE_CURRENT_SOURCE_DIR}/lib2.cpp)
target_include_directories(cmake_lib INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
        )

install(FILES lib2.h DESTINATION include )
