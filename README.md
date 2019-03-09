# darknet

这是经过catkin_make之后的darknet，但是不包括经过训练过后的网络权重。

**在网上其他github上下载的代码可能会遇到各种各样的问题**

##参考github

darknet_ros源代码 ： [leggedrobotics / darknet_ros](https://github.com/leggedrobotics/darknet_ros "darknet_ros源代码")

我下载的源代码github地址及参考blog：[源代码](https://github.com/I-am-Unique/catkin_darknet )  [BLOG](https://blog.csdn.net/m0_38087936/article/details/85849748)

## 需要修改的地方

在catkin_darknet/src/darknet_ros/darknet_ros/config/目录下，ros.yaml文件定义了该工程订阅的topic以及它检测完成以后将结果发布出去的topic 

将其中的  **subscribers**  改为

```python
subscribers:

  	camera_reading:

    	topic: /usb_cam/image_raw

    	queue_size: 1

```

运行方式

```python
roscore
 
roslaunch usb_cam usb_cam-test.launch
 
roslaunch darknet_ros darknet_ros.launch
```













