
add_custom_command (
    OUTPUT LoginSession.cpp User.cpp
    COMMAND ${YBORM_ROOT}/bin/yborm_gen --domain ${PROJECT_SOURCE_DIR}/src/auth_schema.xml
        ${CMAKE_CURRENT_BINARY_DIR}
    DEPENDS ${PROJECT_SOURCE_DIR}/src/auth_schema.xml
)

add_custom_target (generate_domain DEPENDS
    ${CMAKE_CURRENT_BINARY_DIR}/LoginSession.cpp)

