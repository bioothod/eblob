add_library(eblob_python SHARED eblob_python.cpp)
target_link_libraries(eblob_python eblob eblob_cpp ${EBLOB_PYTHON_LIBRARIES})

set_target_properties(eblob_python PROPERTIES
    VERSION ${EBLOB_VERSION}
    SOVERSION ${EBLOB_VERSION_ABI}
)

install(TARGETS eblob_python
    LIBRARY DESTINATION lib${LIB_SUFFIX}
    ARCHIVE DESTINATION lib${LIB_SUFFIX}
    BUNDLE DESTINATION library
)
