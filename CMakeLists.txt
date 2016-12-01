cmake_minimum_required(VERSION 2.8.3)
project(rgbd_srvs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  sensor_msgs
  message_generation
)

add_service_files(
    FILES
    rgbd_image.srv
)

generate_messages(
   DEPENDENCIES
   sensor_msgs
   std_msgs
)

catkin_package(
   CATKIN_DEPENDS message_runtime
)

include_directories(${catkin_INCLUDE_DIRS})
