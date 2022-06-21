cmake_minimum_required(VERSION 3.0.0)
project(socket VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(client tcpcliserv/tcpcli01.c)
add_executable(server tcpcliserv/tcpserv01.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
# link_directories(lib)
target_link_libraries(client libunp.a)
target_link_libraries(server libunp.a)
