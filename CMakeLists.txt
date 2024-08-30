cmake_minimum_required(VERSION 3.3)
set(CMAKE_CXX_STANDARD 14)
project(asvcommonmsg)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(builtin_interfaces REQUIRED)

## Generate added messages and services with any dependencies listed here
rosidl_generate_interfaces( asvcommonmsg
        "msg/DesiredStateForRobot.msg"
        "msg/StateRobotForEvaluation.msg"
        "msg/StateOfBlueRov.msg"

        "srv/ResetEkf.srv"
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()





