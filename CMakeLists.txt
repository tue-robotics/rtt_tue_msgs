cmake_minimum_required(VERSION 2.8.3)
project(rtt_tue_msgs)

find_package(catkin REQUIRED COMPONENTS
  rtt_roscomm
  rtt_actionlib_msgs
  rtt_geometry_msgs
  rtt_std_msgs
  tue_msgs
)

ros_generate_rtt_typekit(tue_msgs)
ros_generate_rtt_service_proxies(tue_msgs)

orocos_generate_package(
  DEPENDS tue_msgs
  DEPENDS_TARGETS rtt_roscomm rtt_actionlib_msgs rtt_geometry_msgs rtt_std_msgs
)
