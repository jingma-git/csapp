cmake_minimum_required(VERSION 3.10)
project(csapp)

include_directories(./include)
add_subdirectory(src)

add_executable(echoserverp conc/echoserverp.c conc/echo.c)
target_link_libraries(echoserverp csapp)



add_executable(echoclient netp/echoclient.c)
target_link_libraries(echoclient csapp)