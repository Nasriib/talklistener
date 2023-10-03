# check_off_2
Talker and Listener
git clone https://github.com/ros2/demos/ 
git pull
Delete all other files and keep demo_nodes_py folders as shown below
Run setup program update
python3 -m pip install setuptools==58.2.0
mkdir -p ros2_ws/src
cd ros2_ws/src
git clone -b humble https://github.com/ros2/demos/  humbledemos
cd ..
colcon build note if don't work use one under  
colcon build --allow-overriding demo_nodes_py
make talker
source ./install/setup.bash
ros2 run demo_nodes_py talker
new terminal
cd ros2_ws/
source ./install/setup.bash
make listener
ros2 run demo_nodes_py listener
open the third terminal for rqt_graph
export DISPLAY=:0
cd ros2_ws/
source ./install/setup.bash
rqt_graph
