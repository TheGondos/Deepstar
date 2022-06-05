add_library(Depot1 SHARED
    Depot1.cpp
    ../BaseDepot.cpp
)

target_include_directories(Depot1 PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(Depot1
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(Depot1
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME Depot1
)

install(TARGETS Depot1
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
