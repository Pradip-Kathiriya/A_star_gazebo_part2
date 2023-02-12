## Project Description
In this project, I have implemented A\* algorithm for path planning for turtlebot3. I have used ROS and Gazebo simulation for implementation of the algorithm.
The environment has a static obstacle which are defined using half plane method. The algorithm has to avoid the obstacles and taking into the account nonholonomic
constraint imposed by the turtlebot3.

## Results



## How to run code?

#### FIRST TERMINAL WINDOW
- Copy the package 'turtlebot3_a_star',into the 'src' folder of a catkin workspace(say 'catkin_ws') which contains other turtlebot3 packages. 
- Use catkin_make or catkin build, depending upon what was used to build that workspace with turtlebot3 packages.
- Source the workspace using
  ```
  devel/setup.bash
  ```

* In the terminal, launch gazebo using the command ('X','Y' and 'Z' should be replaced)
  ```
  roslaunch turtlebot3_a_star a_star.launch x_pos:=X y_pos:=Y z_pos:=Z
  ```
      - replace 'X' with values inbetween 0 and 10 . (in metres) 
      - replace 'Y' with values inbetween 0 and 10 . (in metres)       
      - replace 'Z' with values inbetween 0 and 360 . (in degrees)

#### SECOND TERMINAL WINDOW      
-  Open Second terminal window and navigate to 'test.py' 
  ```
  cd catkin_ws/src/turtlebot3_a_star/src 
  ```
- And run the command:
```
   python test.py   
 ```
   
-  Enter data as prompted( start and goal node).
- The start node should have same values as of 'X' , 'Y' and 'Z', as in roslaunch command. 
- Make sure to enter integer values when asked for, and the value of orientation for start should be in degrees.
- For start and goal positions:
        First, input the x - coordinate and press "Enter" .Followed by inputing the y-coordinate and press "Enter"  
##### 'VERY IMPORANT NOTE' ########     
'RUN THE PROGRAM FROM START AGAIN, WHEN PROMPTED' (This is to respawn the bot correctly in gazebo, as the start or goal position is in obstacle space) 
