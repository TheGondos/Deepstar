add_library(Lander SHARED
Lander.cpp
)

target_include_directories(Lander PUBLIC
	${ORBITER_SOURCE_SDK_INCLUDE_DIR}
    ${ORBITER_BINARY_SDK_DIR}/include
    ${ORBITER_BINARY_SDK_DIR}/XRSound
)

target_link_libraries(Lander
	${ORBITER_SDK_LIB}
    UCSO_API
    XRSound_dll
)

set_target_properties(Lander
	PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${ORBITER_BINARY_MODULE_DIR}/Deepstar
	OUTPUT_NAME Lander
)

install(TARGETS Lander
#	RUNTIME
	DESTINATION ${ORBITER_INSTALL_MODULE_DIR}/Deepstar
)
