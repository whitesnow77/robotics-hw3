cmake_minimum_required(VERSION 2.8.3)
project(topic_custom)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  rospy
  std_msgs
)


add_message_files(
  FILES
  define.msg
)

add_service_files(
  FILES
  AddTwoNum.srv
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)
catkin_package(
  CATKIN_DEPENDS geometry_msgs rospy std_msgs
)
