cmake_minimum_required(VERSION 2.6)
file(TO_CMAKE_PATH "$ENV{IMAGINEPP_ROOT}/CMake" p)
list(APPEND CMAKE_MODULE_PATH "${p}") #For old Imagine++
list(APPEND CMAKE_SYSTEM_FRAMEWORK_PATH /Library/Frameworks) #Mac, why not auto?
find_package(Imagine REQUIRED)

set(SRCS
    ../Game.cpp 
    ../Game.h
    ../Agent.cpp
    ../Agent.h)

project(Puissance4)
add_executable(Puissance4 ${SRCS} Puissance4.cpp Puissance4.h)
ImagineUseModules(Puissance4 LinAlg Images)

