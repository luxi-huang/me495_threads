cmake_minimum_required(VERSION 2.8.3)
project(me495_threads)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)


catkin_python_setup()

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES me495_threads
  CATKIN_DEPENDS std_msgs
#  DEPENDS system_lib
)


install(PROGRAMS
   nodes/sub_thread
   scripts/gil_two_threads.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

