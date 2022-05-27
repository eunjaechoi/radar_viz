cmake_minimum_required(VERSION 2.8.3)
project(sc_can_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
  message_generation
)

add_message_files(FILES Can.msg Ultrasonic.msg CarInfo.msg Radar.msg)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS std_msgs roscpp
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)