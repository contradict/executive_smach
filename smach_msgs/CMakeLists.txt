cmake_minimum_required(VERSION 2.8.3)
project(smach_msgs)

find_package(catkin REQUIRED
    COMPONENTS
        message_generation
        std_msgs
        )

# messages
add_message_files(
    DIRECTORY msg
    FILES
        SmachContainerInitialStatusCmd.msg
        SmachContainerStatus.msg
        SmachContainerStructure.msg
)

generate_messages(
    DEPENDENCIES
        std_msgs
)

catkin_package()
