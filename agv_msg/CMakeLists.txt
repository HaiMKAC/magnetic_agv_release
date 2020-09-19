cmake_minimum_required(VERSION 2.8.3)
project(agv_msg)

find_package(catkin REQUIRED COMPONENTS
    roscpp
    rospy
    std_msgs
    geometry_msgs
    message_generation
)
add_service_files(
    FILES
    DataCheck.srv
)
add_message_files(
    FILES  
    FollowLineSensor.msg
    FollowLineControl.msg
    DiffDriverMotorSpeed.msg
    ArduinoIO.msg
    HmiControl.msg
    BasicFunction.msg
    CardWithFunction.msg
    DataChanged.msg
    CardID.msg
    SafetyStt.msg
    SafetyControl.msg
)
generate_messages(
    DEPENDENCIES
    std_msgs
    # geometry_msgs
)
catkin_package(
    CATKIN_DEPENDS
    std_msgs
    message_runtime
    # geometry_msgs
)