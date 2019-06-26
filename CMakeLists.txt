cmake_minimum_required(VERSION 2.8.3)
project(mummer_navigation_config)

find_package(catkin REQUIRED COMPONENTS
)

catkin_package(
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# install
foreach(dir morse_pr2_launch morse_pr2_move_base_config)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
