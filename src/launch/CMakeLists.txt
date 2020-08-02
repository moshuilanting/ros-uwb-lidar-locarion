cmake_minimum_required(VERSION 2.8.3)
project(launch)


find_package(catkin REQUIRED COMPONENTS
    roscpp std_msgs
    )




catkin_package(
    #  INCLUDE_DIRS include
    #  LIBRARIES launch
    #  CATKIN_DEPENDS roscpp std_msgs
    #  DEPENDS system_lib
    )


include_directories(
    # include
    ${catkin_INCLUDE_DIRS}
    )


#install(DIRECTORY controller/
#    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/controller
#    )

#install(DIRECTORY
#    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
#    )
