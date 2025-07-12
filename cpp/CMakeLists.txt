cmake_minimum_required(VERSION 3.12.0) # older would work, but could give warnings on policy CMP0074
project(PETSIRDUseCaseTemplate VERSION 0.7.2)

set(CMAKE_CXX_STANDARD 17)

#Set the build type to Release if not specified
if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release CACHE STRING
            "Choose the type of build, options are: None Debug Release RelWithDebInfo MinSizeRel."
            FORCE)
endif ()

if(WIN32)
  add_compile_options(/W3 /WX)
else()
  add_compile_options(-Wall -Wextra -pedantic)
endif()

set(PETSIRD_dir ../PETSIRD/cpp/generated)
add_subdirectory(${PETSIRD_dir} PETSIRD_generated)

# Add any packages, below is an example for ROOT (unlikely you'll need that one though!)
# find_package(ROOT REQUIRED COMPONENTS Tree)

# Example lines for a new executable
# add_executable(my_prog my_prog.cpp)
# target_include_directories(my_prog PUBLIC ${PETSIRD_dir})
# needed for helpers
# target_include_directories(my_prog PUBLIC ${PETSIRD_dir}/..)
# target_include_directories(my_prog PUBLIC ${PETSIRD_dir}/../helpers/include)
# target_link_libraries(my_prog PUBLIC petsird_generated)

# add any dependencies on packages here
# target_link_libraries(my_prog PUBLIC ROOT::Tree)

# install(TARGETS my_prog DESTINATION bin)
