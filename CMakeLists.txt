cmake_minimum_required(VERSION 2.8.3)
project(rosruby_messages)
find_package(catkin REQUIRED COMPONENTS rosruby genrb message_generation)

catkin_package(
  DEPENDS rosruby rosruby_actionlib message_runtime
  )

rosruby_setup()

# please avoid metapackage!
rosruby_generate_messages(ackermann_msgs
#actionlib_msgs # installed by rosruby_actionlib
arbotix_msgs
audio_common_msgs
calibration_msgs
cob_srvs
#common_msgs # no message (metapackage)
concert_msgs
control_msgs
controller_manager_msgs
diagnostic_msgs
dynamixel_msgs
gateway_msgs
gazebo_msgs
geographic_msgs
#geometry_msgs # installed by rosruby
hector_nav_msgs
hector_worldmodel_msgs
household_objects_database_msgs
kingfisher_msgs
kobuki_msgs
manipulation_msgs
map_msgs
move_base_msgs
moveit_msgs
multimaster_msgs_fkie
nav_msgs
nmea_msgs
object_recognition_msgs
octomap_msgs
pcl_msgs
pr2_controllers_msgs
pr2_mechanism_msgs
pr2_msgs
rocon_app_manager_msgs
#rocon_msgs # no message (metapackage)
#rosgraph_msgs # installed by rosruby
rosserial_msgs
sensor_msgs
shape_msgs
smach_msgs
sr_ronex_msgs
#std_msgs #installed by rosruby
std_srvs
stereo_msgs
#tf2_geometry_msgs # no messages
tf2_msgs
trajectory_msgs
turtlebot_msgs
underwater_sensor_msgs
uuid_msgs
velodyne_msgs
visualization_msgs
yocs_msgs
zeroconf_msgs)
