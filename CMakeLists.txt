cmake_minimum_required(VERSION 2.8.3)
project(aicrobo_tutorials)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs)

## Declare a catkin package
catkin_package()

## Build talker and listener
include_directories(${catkin_INCLUDE_DIRS})

add_executable(talker nodes/talker.cpp)
target_link_libraries(talker ${catkin_LIBRARIES})

add_executable(listener nodes/listener.cpp)
target_link_libraries(listener ${catkin_LIBRARIES})