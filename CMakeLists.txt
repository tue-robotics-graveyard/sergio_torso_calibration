cmake_minimum_required(VERSION 2.8.3)
project(quaternion_to_euler)

find_package(catkin REQUIRED COMPONENTS
	rospy
	std_msgs
	message_generation
)

# find_package(Boost REQUIRED COMPONENTS system program_options)
# find_package(PCL REQUIRED)
# find_package(OpenCV REQUIRED)

# ------------------------------------------------------------------------------------------------
#                                     ROS MESSAGES AND SERVICES
# ------------------------------------------------------------------------------------------------

# Generate messages
 add_message_files(
    FILES Eulers.msg
    DIRECTORY msg
 )

# Generate services
# add_service_files(
#    FILES
#    service1.srv
#    ...
# )

# Generate added messages and services with any dependencies listed here
 generate_messages(
	DEPENDENCIES std_msgs
 )

# ------------------------------------------------------------------------------------------------
#                                          CATKIN EXPORT
# ------------------------------------------------------------------------------------------------

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES bla
  CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)

# ------------------------------------------------------------------------------------------------
#                                              BUILD
# ------------------------------------------------------------------------------------------------

include_directories(
    include
    ${catkin_INCLUDE_DIRS}
)

# add_library(library_name
#     src/lib_source_file1.cpp
#     ...
# )
# target_link_libraries(library_name ${catkin_LIBRARIES})

# add_executable(exec_name
#     src/source_file1.cpp
#     ...
# )
# target_link_libraries(exec_name ${catkin_LIBRARIES})


