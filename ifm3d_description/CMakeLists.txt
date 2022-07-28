cmake_minimum_required(VERSION 3.0.2)
project(ifm3d_description)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY cfg launch meshes urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(tests/roslaunch_test_o3r255.xml)
endif()
