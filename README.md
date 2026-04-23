pour lancer gazebo 
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
pour lancer slam 
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
ajoute :
    • Map 
    • LaserScan
pour controle le turtukboot
ros2 run turtlebot3_teleop teleop_keyboard
pour sauvgarder la carte 
ros2 run nav2_map_server map_saver_cli -f ~/map
Navigation autonome
Lancer avec ta carte
ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=True map:=~/map.yaml
Dans RViz
clique sur :2D Goal Pose 
choisis un point
le robot va :
    • planifier 
    • éviter obstacles 
    • atteindre la cible
