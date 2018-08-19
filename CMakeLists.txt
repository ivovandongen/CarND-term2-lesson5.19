cmake_minimum_required(VERSION 3.10)
project(CarND_term2_lesson5_19)

set(CMAKE_CXX_STANDARD 14)

include(deps/eigen.cmake)

if (UNIX)
    # Silence warnings in Eigen
    add_compile_options(-Wno-deprecated-register)
endif()



add_executable(Jacobian
    ${CMAKE_SOURCE_DIR}/src/main.cpp
)

target_link_libraries(Jacobian Eigen)
