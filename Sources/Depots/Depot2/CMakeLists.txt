add_library(Depot2 SHARED
Depot2.cpp
    ../BaseDepot.cpp
)

target_include_directories(Depot2 PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(Depot2
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(Depot2
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME Depot2
)

install(TARGETS Depot2
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
