cmake_minimum_required(VERSION 2.8.3)
project(webui)
find_package(catkin REQUIRED COMPONENTS web_msgs roslib rospy rosservice launchman pyclearsilver std_msgs std_srvs diagnostic_msgs rosweb ros_apache2)

# include_directories(include ${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})## Generate added messages and services with any dependencies listed here
#generate_messages(
#    #TODO DEPENDENCIES geometry_msgs std_msgs
#)

# catkin_package parameters: http://ros.org/doc/groovy/api/catkin/html/dev_guide/generated_cmake_api.html#catkin-package
# TODO: fill in what other packages will need to use this package
catkin_package(
    DEPENDS 
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(DIRECTORY launch scripts src varwww DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(FILES apache.cfg install_root install.py install.pyc setup.bash setup.bash.in setup.make webui.init apache.cfg.in DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
