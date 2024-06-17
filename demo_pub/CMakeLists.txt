cmake_minimum_required(VERSION 3.0.2)
project(demo_pub)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  geometry_msgs
  std_srvs
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(PROGRAMS
  scripts/shutdown_service.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

