cmake_minimum_required(VERSION 2.8.3)
project(hello_robot)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  sensor_msgs
  riki_msgs
  std_msgs
  tf
)
catkin_package(
  INCLUDE_DIRS include
  LIBRARIES clbrobot
  CATKIN_DEPENDS roscpp rospy tf nav_msgs riki_msgs geometry_msgs sensor_msgs std_msgs 
)

###########
## Build ##
###########

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_library(${PROJECT_NAME}_lib src/riki_base.cpp)
add_executable(${PROJECT_NAME} src/riki_base_node.cpp)
target_link_libraries(${PROJECT_NAME} ${PROJECT_NAME}_lib ${catkin_LIBRARIES})

