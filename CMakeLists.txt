
cmake_minimum_required (VERSION 3.17)

project(project_1)

include(cmake/CPM.cmake)

find_package(MPI REQUIRED)

add_library(project_1 heat_mpi.cxx)

link_libraries(project_1)

include(CTest)

#add_executable(heat heat.c)
#target_link_libraries(heat PRIVATE MPI::MPI_CXX)

#add_executable(functions functions.c)
#target_link_libraries(functions PRIVATE MPI::MPI_CXX)

add_executable(heat_mpi heat_mpi.cxx)
target_link_libraries(heat_mpi PRIVATE MPI::MPI_CXX)

