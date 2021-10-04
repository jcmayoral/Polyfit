cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(polyfit_cpp)

add_compile_options(-std=c++17)

include_directories(include)

link_directories(${Boost_INCLUDE_DIRS})

#add_library(dynobjectgazebo SHARED src/gazebo/dynamic_object_gazebo_interface.cpp)
#target_link_libraries(dynobjectgazebo ${GAZEBO_LIBRARIES} ${roscpp_LIBRARIES})

#add_dependencies(dynobjectros   ${gr_action_msgs_EXPORTED_TARGETS})
#add_library(${PROJECT_NAME} src/polyfit_boost.cpp)
#target_link_libraries(rosinterface ${roscpp_LIBRARIES} ${dynamic_reconfigure_LIBRARIES} ${actionlib_LIBRARIES})

add_executable(polyfit_cpp_example src/example.cpp)
target_link_libraries(polyfit_cpp_example)
#include(FindBoost)
#  find_package(Boost ${MIN_BOOST_VERSION} REQUIRED system filesystem regex)
#target_link_libraries(ros_interface_node ${GAZEBO_LIBRARIES} rosinterface ${tf2_ros_LIBRARIES})

install(TARGETS ${PROJECT} 
	PUBLIC_HEADER DESTINATION /home/jose/blabla)
