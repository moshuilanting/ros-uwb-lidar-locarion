cmake_minimum_required(VERSION 3.0.2)
project(my_pcl_tutorial)


find_package(catkin REQUIRED COMPONENTS
  pcl_conversions
  pcl_ros
  roscpp
  sensor_msgs
)


find_package(PCL REQUIRED)
catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)


link_directories(${PCL_LIBRARY_DIRS})


add_executable(example src/example.cpp)
target_link_libraries(example ${catkin_LIBRARIES})

add_executable(pcl_creat src/pcl_creat.cpp)
target_link_libraries(pcl_creat ${catkin_LIBRARIES})

add_executable(pcl_read src/pcl_read.cpp)
target_link_libraries(pcl_read ${catkin_LIBRARIES})

add_executable(pcl_write src/pcl_write.cpp)
target_link_libraries(pcl_write ${catkin_LIBRARIES})

add_executable(cloud_viewer src/cloud_viewer.cpp)
target_link_libraries(cloud_viewer ${catkin_LIBRARIES} ${PCL_LIBRARIES})
