cmake_minimum_required(VERSION 2.8.12)

project(nlu_msgs)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS}")

find_package(catkin REQUIRED
  COMPONENTS
    std_msgs
    message_generation
)

add_message_files(
  FILES
    GroundedAction.msg
    GroundedActionParam.msg
)

generate_messages(
  DEPENDENCIES
    #actionlib_msgs
    #geometry_msgs
    #sensor_msgs
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    #actionlib_msgs
    #geometry_msgs
    #sensor_msgs
    message_runtime
    std_msgs
)
