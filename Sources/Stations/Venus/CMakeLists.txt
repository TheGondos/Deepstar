add_library(VenusStation SHARED
    VenusStation.cpp
    ../BaseStation.cpp
)

target_include_directories(VenusStation PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(VenusStation
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(VenusStation
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME VenusStation
)

install(TARGETS VenusStation
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
