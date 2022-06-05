add_library(Aerolander SHARED
    Aerolander.cpp
)

target_include_directories(Aerolander PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(Aerolander
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(Aerolander
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME Aerolander
)

install(TARGETS Aerolander
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
