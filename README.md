![Screenshot](/map.png)

All sources were taken from [ROS documentation](http://docs.ros.org/indigo/api/loam_velodyne/html/files.html)



**How to build with catkin**

Build `loam_velodyne`:

```
$ cd ~/catkin_ws/src/
$ git clone git@github.com:Tenant/loam_velodyne.git
$ cd ~/catkin_ws
$ catkin_make -DCMAKE_BUILD_TYPE=Release 
$ source ~/catkin_ws/devel/setup.bash
```

Build `velodyne`:

```basj
$ cd ~/catkin_ws/src/
$ git clone git@github.com:Tenant/velodyne.git
$ cd ~/catkin_ws
$ catkin_make --only-pkg-with-deps velodyne -DCMAKE_BUILD_TYPE=Release
$ source ~/catkin_ws/devel/setup.sh
```

Build `fixed_tf_broadcaster`:

```
$ cd ~/catkin_ws/src/
$ git clone git@github.com:Tenant/fixed_tf_broadcaster.git
$ cd ~/catkin_ws
$ source ~/catkin_ws/devel/setup.sh
```



**Running**:

The path of data is defined in start_*.launch

```
roslaunch fixed_tf_broadcaster start_201.launch
```


```
roslaunch fixed_tf_broadcaster start_campus1.launch
```


```
roslaunch fixed_tf_broadcaster start_campus2.launch
```


