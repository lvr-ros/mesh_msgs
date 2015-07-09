cmake_minimum_required(VERSION 2.8.3)
project(mesh_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  geometry_msgs
  sensor_msgs
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
Material.msg
Cluster.msg
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  sensor_msgs
)

catkin_package(
  INCLUDE_DIRS
  CATKIN_DEPENDS
    roscpp
    geometry_msgs
    sensor_msgs
)
