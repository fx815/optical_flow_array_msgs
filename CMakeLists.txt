cmake_minimum_required(VERSION 2.8.3)
project(optical_flow_array_msgs)

find_package(catkin REQUIRED COMPONENTS std_msgs message_generation)
include_directories(include ${catkin_INCLUDE_DIRS})

find_package(cmake_modules REQUIRED)
 

add_message_files(
  FILES
  optical_flow_array.msg
)

#add_service_files(
 # FILES
  #PlannerService.srv
  #PolygonService.srv
#)

generate_messages(
  DEPENDENCIES std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
