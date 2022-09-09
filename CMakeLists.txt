cmake_minimum_required(VERSION 3.0.2)
project(labvirtual_messages)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

# Generate messages in the 'msg' folder
add_message_files(
  FILES
  Sensor5TEMessage.msg
)

# Generate services in the 'srv' folder
add_service_files(
  FILES
  Sensor5TE.srv
)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime 
  )

include_directories(
  ${catkin_INCLUDE_DIRS}
)

