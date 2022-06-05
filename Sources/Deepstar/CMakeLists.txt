add_library(Deepstar SHARED
Deepstar.cpp
)

target_include_directories(Deepstar PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(Deepstar
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(Deepstar
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME Deepstar
)

install(TARGETS Deepstar
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
