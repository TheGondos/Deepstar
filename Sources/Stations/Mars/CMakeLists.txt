add_library(MarsStation SHARED
    MarsStation.cpp
    ../BaseStation.cpp
)

target_include_directories(MarsStation PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(MarsStation
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(MarsStation
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME MarsStation
)

install(TARGETS MarsStation
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
