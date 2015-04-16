cmake_minimum_required(VERSION 2.8.3)
project(mesh_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
PolygonIndices.msg
PolygonMesh.msg
PolygonMeshStamped.msg
TriangleIndices.msg
TriangleMesh.msg
TriangleMeshStamped.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs geometry_msgs
)

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS
    roscpp
    std_msgs
    geometry_msgs
)
