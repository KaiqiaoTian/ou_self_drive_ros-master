cmake_minimum_required(VERSION 2.8.3)
project(sign_detection)

find_package(catkin REQUIRED COMPONENTS
  actionlib
  cv_bridge
  image_transport
  pcl_ros
  roscpp
  rospy
  sensor_msgs
  std_msgs
  tf
)

add_message_files(
  FILES
  SignData.msg
  SignDataArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package()
