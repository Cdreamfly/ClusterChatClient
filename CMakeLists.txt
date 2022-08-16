cmake_minimum_required(VERSION 3.16)
project(ClusterChatClient)

set(CMAKE_CXX_STANDARD 17)

include_directories(include)
#指定生成可执行文件
add_executable(ClusterChatClient client.cpp src/model/user.cpp src/model/group.cpp src/model/groupuser.cpp)
#指定可执行文件链接时需要依赖的库文件
target_link_libraries(ClusterChatClient pthread)