project(Growing)
cmake_minimum_required(VERSION 2.6)

#######################
# Growing Registration plugin

set (CLP Growing)
set (${CLP}_SOURCE ${CLP}.cxx)
generateclp(${CLP}_SOURCE ${CLP}.xml)

add_executable(${CLP} ${${CLP}_SOURCE})
target_link_libraries(${CLP} ${ITK_LIBRARIES})

