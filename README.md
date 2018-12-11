![Screenshot](/map.png)
Sample map built from [nsh_indoor_outdoor.bag](http://www.frc.ri.cmu.edu/~jizhang03/Datasets/nsh_indoor_outdoor.bag) (opened with [ccViewer](http://www.danielgm.net/cc/))

:white_check_mark: Tested with ROS Indigo and Velodyne VLP16. [(Screencast)](https://youtu.be/o1cLXY-Es54)

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

```
roslaunch fixed_tf_broadcaster startall.launch
```


