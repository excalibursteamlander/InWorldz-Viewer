# -*- cmake -*-

project(iw_imagebase)

include_directories(
	${IW_IMAGEBASE_INCLUDE_DIRS}
    )

set(iw_imagebase_SOURCE_FILES
    imagebaseforkdu.cpp
    )

set(iw_imagebase_HEADER_FILES
    CMakeLists.txt

    imagebaseforkdu.h
    )

set_source_files_properties(${iw_imagebase_HEADER_FILES}
                            PROPERTIES HEADER_FILE_ONLY TRUE)

list(APPEND iw_imagebase_SOURCE_FILES ${iw_imagebase_HEADER_FILES})

add_library (iw_imagebase ${iw_imagebase_SOURCE_FILES})
