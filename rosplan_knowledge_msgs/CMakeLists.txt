cmake_minimum_required(VERSION 2.8.3)
project(rosplan_knowledge_msgs)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  message_generation
  diagnostic_msgs
  roscpp
  rospy
  std_msgs
  genmsg
)

## Generate messages in the 'msg' folder
add_message_files(
   FILES
   Filter.msg
   KnowledgeItem.msg
   Notification.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  AttributeService.srv
  InstanceService.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
   DEPENDENCIES
   diagnostic_msgs
   std_msgs
)

## Declare a catkin package
catkin_package()

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)