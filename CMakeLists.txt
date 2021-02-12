cmake_minimum_required(VERSION 3.2.0)
project(gazebo_rad_resources)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
)

find_package(gazebo REQUIRED)

catkin_package(
  DEPENDS gazebo_ros
  # CATKIN_DEPENDS
  )

include_directories(
  include
  ${GAZEBO_INCLUDE_DIRS}
  ${CMAKE_CURRENT_BINARY_DIR}
  ${catkin_INCLUDE_DIRS}
  )

link_directories(${GAZEBO_LIBRARY_DIRS})
