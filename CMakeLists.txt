cmake_minimum_required(VERSION 3.0.0)
project(socket VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(socket intro/daytimetcpcli.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
# link_directories(lib)
target_link_libraries(socket libunp.a)
