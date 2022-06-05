add_subdirectory(Sources/Aerolander)
add_subdirectory(Sources/Deepstar)
add_subdirectory(Sources/Depots)
add_subdirectory(Sources/Lander)
add_subdirectory(Sources/Probes)
add_subdirectory(Sources/Spacehab)
add_subdirectory(Sources/Stations)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/Config
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/Meshes
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/Scenarios
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/Textures
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/XRSound
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/Orbiter/Images
    DESTINATION ${ORBITER_INSTALL_ROOT_DIR}/
)
