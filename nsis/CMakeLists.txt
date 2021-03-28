if(CMAKE_SIZEOF_VOID_P EQUAL 8)
    set(VCREDIST_SUFFIX x64)
else()
    set(VCREDIST_SUFFIX x86)
endif()

install(FILES vcredist_msvc2015_${VCREDIST_SUFFIX}.exe
    DESTINATION Drivers
    COMPONENT VcRedist_libs
    RENAME vcredist.exe
)
