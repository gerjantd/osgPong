cmake_minimum_required( VERSION 2.6 )
project( osgPong )
find_package(OpenThreads)
find_package(osg)
find_package(osgDB)
find_package(osgGA)
find_package(osgText)
find_package(osgUtil)
find_package(osgViewer)

macro( config_project PROJNAME LIBNAME )
include_directories( ${${LIBNAME}_INCLUDE_DIR} )
target_link_libraries( ${PROJNAME} ${${LIBNAME}_LIBRARY} )
endmacro()
add_executable(osgPong main.cpp Camera.cpp FindNamedNode.cpp GameController.cpp Player.cpp PongGame.cpp Ball.cpp RealPlayer.cpp PlayerScore.cpp PongScore.cpp)
config_project(osgPong OPENTHREADS )
config_project(osgPong OSG )
config_project(osgPong OSGDB )
config_project(osgPong OSGGA )
config_project(osgPong OSGTEXT )
config_project(osgPong OSGUTIL )
config_project(osgPong OSGVIEWER )
config_project(osgPong Player )
config_project(osgPong Camera )
config_project(osgPong FindNamedNode )
config_project(osgPong GameController )
config_project(osgPong RealPlayer )
config_project(osgPong PongGame )
config_project(osgPong Ball )
config_project(osgPong PlayerScore )
config_project(osgPong PongScore )

