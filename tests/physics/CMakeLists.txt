find_package(Boost COMPONENTS program_options filesystem system REQUIRED)

add_executable(moist_thermal moist_thermal.cpp)
target_link_libraries(moist_thermal ${HDF5_LIBRARIES})
target_include_directories(moist_thermal PUBLIC ${HDF5_INCLUDE_DIRS})
target_link_libraries(moist_thermal ${Boost_LIBRARIES})
add_test(moist_thermal moist_thermal ${CMAKE_BINARY_DIR})
