cmake_minimum_required(VERSION 3.0.0)
project(Asteroids VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(CTest)
enable_testing()

link_libraries(-lX11 -lGL -lpthread -lpng -lstdc++fs)
include_directories(include)

file(GLOB TARGET_SRC "./src/*.cpp" )


add_executable(main ${TARGET_SRC} include/olcPixelGameEngine.h)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
