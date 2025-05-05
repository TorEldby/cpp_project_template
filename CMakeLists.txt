cmake_minimum_required(VERSION 4.0)
project(TemplateProject VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_TOOLCHAIN_FILE "${VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake")

file(GLOB INCLUDE "include/*.h")
file(GLOB SOURCES "src/*.cpp")

add_executable(${PROJECT_NAME} ${INCLUDE} ${SOURCES})