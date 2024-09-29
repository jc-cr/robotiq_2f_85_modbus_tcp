cmake_minimum_required(VERSION 3.0.2)
project(robotiq_2f_85_modbus_tcp)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  std_srvs
)

catkin_package(
  CATKIN_DEPENDS rospy std_msgs std_srvs
)


catkin_install_python(PROGRAMS 
  scripts/robotiq_2f_85_modbus_tcp_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)