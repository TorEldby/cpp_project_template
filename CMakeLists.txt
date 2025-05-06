cmake_minimum_required(VERSION 4.0)


set(VCPKG_MANIFEST_MODE OFF)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(TemplateProject VERSION 1.0.0)

file(GLOB INCLUDE "include/*.h")
file(GLOB SOURCES "src/*.cpp")

add_executable(${PROJECT_NAME} ${INCLUDE} ${SOURCES})

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(${PROJECT_NAME} PRIVATE glfw)

find_package(glad CONFIG REQUIRED)
target_link_libraries(${PROJECT_NAME} PRIVATE glad::glad)