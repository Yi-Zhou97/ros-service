# 创建server端
## 创建好srv
创建srv,并且注意xml和cmakelist文件的编写。 参考<http://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv#Creating_a_srv>
## call back function 
```
bool function_name(package_name::service_name::request &req, package_name::service_name::response &res)
{
与下位机的通信，例如tcp通信可以在call back function中实现，发送req中的消息
}
```
## 初始化ros
```ros::init("node_name")；```
## 初始化句柄
```ros::NodeHandle node；```
## 发布service
```ros::ServiceServer service = node.advertiseService("service_name", call back function);```
