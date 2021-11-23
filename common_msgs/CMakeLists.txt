make_minimum_required(VERSION 2.8.3)
project(common_msgs)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  rospy
  std_msgs
)

# Generate services in the 'srv' folder
add_service_files(
  FILES
  AddTwoNum.srv
)

add_message_files(
  FILES
  TimePose.msg
)
# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)
catkin_package(
  CATKIN_DEPENDS rospy std_msgs
)
