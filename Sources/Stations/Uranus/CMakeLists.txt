add_library(UranusStation SHARED
UranusStation.cpp
    ../BaseStation.cpp
)

target_include_directories(UranusStation PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(UranusStation
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(UranusStation
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME UranusStation
)

install(TARGETS UranusStation
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
