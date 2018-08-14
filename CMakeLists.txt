cmake_minimum_required(VERSION 3.5.1)
project(thudhcp)

include_directories(
  include
)


add_library(interface
  src/interface.c)

add_library(dhcp
  src/dhcp.c)

add_library(socket
  src/socket.c)

add_executable(main
  src/main.c)

target_link_libraries( main
  interface
  dhcp
  socket
)
