cmake_minimum_required(VERSION 3.8)
project(right_arm_walter)

find_package(ament_cmake REQUIRED)

foreach(dir config launch meshes urdf)
  if(EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/${dir}")
    install(
      DIRECTORY ${dir}/
      DESTINATION share/${PROJECT_NAME}/${dir}
    )
  endif()
endforeach()

ament_package()

