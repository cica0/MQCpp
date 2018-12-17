cmake_minimum_required(VERSION 2.8.0)
project("mineMQ")

set(CMAKE_CXX_FLAGS "-g -Wall -std=c++11")
set(CMAKE_CXX_FLAGS_DEBUG  "-O0")    

include_directories(
  "${CMAKE_CURRENT_SOURCE_DIR}/include"
  "${CMAKE_CURRENT_SOURCE_DIR}/src"
  )

link_directories(
  "${CMAKE_CURRENT_SOURCE_DIR}/lib"
  )

aux_source_directory(./src SRCS)
aux_source_directory(./src/broker SRCS)
aux_source_directory(./src/producer SRCS)
aux_source_directory(./src/consumer SRCS)

add_executable(${PROJECT_NAME} ${SRCS})

target_link_libraries(${PROJECT_NAME} 
    )
