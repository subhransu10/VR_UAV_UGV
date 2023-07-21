# Uniting UAV and UGV for Efficient Pollution Inspection
 <img src="https://user-images.githubusercontent.com/62358773/158238820-f418cc09-4227-4afc-9c31-1705dfb64f5a.png" width="5%" height="5%"> Professor Gianni Viardo Vercelli <img src="https://user-images.githubusercontent.com/62358773/158238810-c5dcb486-ba24-4b35-87de-39a54e88f36b.png" width="5%" height="5%"> Student: [Subhransu Sourav Priyadarshan](https://github.com/subhransu10)
 
 ## Aim of the Project
The goal of the project is to inspect a natural area for pollutants risk. In order to achieve this task, we need
a UAV and a UGV. The UAV patrols the environment checking the pollutants level in the atmosphere when it
exceeds a threshold value, it sends a notification for the action that needs to be taken in order to handle the
situation and then it lands on the UGV. Both drones move autonomously in the environment and carry out the
inspection.
The UAV has a camera and a sensor-equipped in order to carry out the inspection and detection process at the
same time. Then it sends a notification in case of an increase in pollutants level. The UGV has a landing pad
for the UAV.

## State of the Art
 Sudarsanan A. et al described the places where humans cannot reach, unmanned Aerial vehicles (UAV) can. Hence, environmental drones
are made for autonomous monitoring, analysis, and countering of air pollution. Various low-cost sensors are
used to measure the humidity, temperature, pressure, wind speed, and precipitation at different heights in a
particular area. Air Quality Index (AQI) is measured by measuring the concentration of different pollutants in
an area. The data from the drone is sent to the base station via wireless communication to the base station for
AQI mapping. The threshold values of the pollutants have already been standardized.
E-drones offer another way to deal with huge-scale air pollutant elimination that will actually automatically
monitor and eliminate pollutants that are effectively present in the atmosphere. This tale approach includes
the utilization of drones to independently screen the air quality in a particular area, distinguish the presence
of any of these toxins, and carry out an appropriate decrease alternative at a particular elevation to guarantee
these pollutants in the atmosphere are removed. The E-drone has been utilized to measure the contamination
convergences of O3, CO, NH3, and PM 2.5.

## Tools - Unreal Engine 5.0
It is the world’s most open and advanced real-time 3D creation tool. We can connect to media production
pipelines, with support for industry standards like FBX, USD, and Alembic. First-class USD support enables
users to collaborate better with team members and work in parallel. Also, in this project, we make use of this
feature.

### Pipeline Integration
+ __FBX Import__: With the help of this feature, we imported the .fbx files into our project. The drone (in
particular) that we used for our project is a.fbx file which is implemented by the FBX support that the
Unreal Engine provides to its users.
+ __Python Scripting__: We were easily able to automate our workflows with full support for the industry-standard Python scripting in the Unreal Editor through Blueprints (be it the UAV flying or UGV movement.
### World Building
+ __The Unreal Editor__: Unreal Engine includes the Unreal Editor, an integrated development environment
available on Linux, macOS, and Windows for content authoring and game-level development.

+ __Landscape and terrain tools__: We created our environment with the help of these features on Unreal
Engine. We could non-destructively edit our landscape with a layer reserved on splines and make changes
in Blueprint.
### Blueprint visual scripting system
With artist-friendly Blueprint visual scripting, we could rapidly prototype and ship interactive content
without touching a line of code. We used Blueprints to build object behaviors and interactions(such as pollutants,
fires, drone movements, etc), adjust input controls, and so much more.
### Content
+ __Marketplace ecosystem__: The Unreal Engine Marketplace has thousands of high-quality assets and
plugins to accelerate production and bring new functionality to your work. We were able to access new
environments, characters, animations, textures, props, sound and visual effects, music tracks, Blueprints,
middleware integration plugins, add-on tools, and full starter kits.
+ __Quixel Megascans__: Every Unreal Engine license comes with free access to the entire Quixel Megascans
library for use in Unreal Engine. Based on real-world scans, this premium-quality library features thousands
of 3D and 2D PBR assets with optimized topology, UVs, and LODs, and consistent scale and resolution.
With Quixel Bridge fully integrated into the Unreal Editor, we could simply drag and drop your selected
Megascans directly into your scene.

## Description
Briefly describing the project, the UAV is supposed to patrol an area inspecting the air quality and
checking the pollution level with the help of a UGV and then further actions will be taken according to the
inspection.
Look below to get a brief idea before getting to know all the components and tasks involved in the project.

### Building the Environment
The environment is a forest environment that we built with the help of some content from the Unreal market-
place and with the help of a number of plugins and other add-ons we were able to create it. The environment has
roads(for the movement of the UGV), it has chopped wood, and fires(we got these from the Unreal Marketplace).

### Components used
+ __Drone(UAV)__: The Drone .fbx that we used is a Phantom4 Pro. It has the ability to carry out the sensor
with a payload.
+ __UGV__ : It is a Drivable M1126 Stryker ICV (West). It can move in any kind of difficult terrain. It has a
nozzle which can also be used to spray in the atmosphere. we use the static mesh component of the
+ __Smoke__: The smoke (which is caused by fire caught on wood)
+ __Fire__: This effect is due to the Niagara plugin on Unreal Engine. We got it from the marketplace and made
some changes according to the task.
+ __Cameras__: There are three cameras used in our project. There is a camera equipped on the drone and
also a camera each to show the point of view of the drone and the UGV.
### Blueprints Used
+ __Drone and its path__: The Blueprint consists of three parts - path reference, flying mechanics, sensory
detection, and alert generation.
+ __UGV and its path__: The blueprint consists of two parts - path reference and movement.
+ Pollutants material (CO2)
## Scenario
There is a fire caused by chopped wood which is releasing harmful substances into the atmosphere(CO2) and
there is smoke due to it and the drone while patrolling, notices that the area around it is not fit for breathing
and it alerts us to take some action that would control the situation.

## Functionalities of the Blueprints
+ __UAV Blueprints__ :
  ### Path reference
  The "EventBeginPlay" function in Unreal Engine's Blueprint scripting is an event that is triggered when the Blueprint actor or object is initially spawned or begins to play in the game world. It serves as a starting point for executing any specific actions or behaviors at the beginning of the actor's lifecycle.

When this event is called, it allows you to perform initialization tasks or set up initial states for the Blueprint actor. It is commonly used to set variables, attach components, spawn other actors, or perform any necessary setup before the actor starts interacting with the game environment or other actors.

To implement the __"EventBeginPlay"__ function in a Blueprint, follow these steps:

1. Open the Blueprint editor for the actor or object you want to add the event to.
2. In the Event Graph, right-click on an empty area and search for "EventBeginPlay".
3. Drag and drop the "EventBeginPlay" node from the search results into the graph.
4. Connect the execution pin (the white arrow) of the "EventBeginPlay" node to the nodes representing the actions or behaviors you want to execute at the beginning of the actor's gameplay.

Here's an example of how the __"EventBeginPlay"__ function can be used in a Blueprint:

1. When the actor spawns or begins playing, the "EventBeginPlay" event is triggered.
2. In the graph, you can add nodes to set the initial values of variables, initialize components, or perform other necessary setup tasks.
3. You can connect additional nodes to the "EventBeginPlay" node to execute specific actions or behaviors based on the actor's initial state or conditions.

It's important to note that the "EventBeginPlay" function is typically executed only once during the actor's lifecycle, at the start of gameplay. If you need to perform actions repeatedly or continuously during gameplay, you may need to use other event functions or custom logic in your Blueprint.

### Flying mechanics
We make a  __“FlyDrone”__  function to make the drone fly. We need to connect nodes to it 
The nodes include 

-	Movement track (which is the path reference)
-	There is a function to input the velocity of the drone
-	We must note that the path reference must be given in this case. In Unreal Engine, the "Set Play Rate" function is used to control the playback speed of a specific animation or audio asset. It allows you to adjust the speed at which the asset plays, enabling you to slow it down, speed it up, or even play it in reverse.
-	NOTE: The path reference must be connected to the drone.

In Unreal Engine, you can use the _"Get Location at Distance Along Spline"_ function to obtain the world location at a specified distance along a spline. This function allows you to retrieve a point along a spline curve based on the distance from the spline's starting point. Here, we have defined certain checkpoints in the map so that it goes from one to the other. So, the functions return the same values as  the checkpoints and help the drone move from one to the other.
Get rotation at distance along the spline – function is used, although it has the same functionality as above it is useful in the camera orientation of the drone.

### Sensory Functionalities
On component begin overlap 
- (It is the sensor) of the drone whose target node is the smoke blueprint. If it doesn’t detect it, then it flies normally. When it flies into the smoke it generates an alarm (as the air quality is poor). Note: the smoke contains CO2 ( we already created a blueprint for it).

+ __UGV Blueprints__
The blueprint for the UGV only has two functionalities which are for path ref and movement as in UAV. Hence, for the same information, you can refer the previous section.

+ __Mapping__
For mapping, we divide  the map into four sections and the box which contains the pollutant can be seen in the mapping (at the end of the solution ) which can be seen from the “light complexity” mode. You can see this in the simulation (Click on the link in the __"Results"__ section). The red color depicts the pollutants at the highest concentration white being the medium concentration and blue depicts clean air.

## Conclusion & Future Improvements
The environment built in Unreal Engine, along with the implemented UAV and UGV blueprints, enables an
autonomous inspection system for natural areas. The system effectively detects and monitors pollutant risks,
generating alerts and providing real-time visuals. The autonomous movement and landing capabilities of the
UAV and UGV contribute to the efficiency and effectiveness of the inspection process.

There can be certain improvements that come to mind which can be done in order to provide a more detailed and effective solution.
1. __Enhance Sensor Capabilities:__ Explore the possibility of integrating additional sensors to detect a wider
range of pollutants.
2. __Intelligent Path Planning:__ Incorporate machine learning algorithms to optimize the inspection path
based on pollutant distribution patterns.
3. __Real-time Data Analysis:__ Implement a data analysis module to provide more in-depth insights and
predictive capabilities based on collected pollutant data using ROS.

## Results
Based on the above-mentioned functionalities and also using the tools of the __Unreal Engine__ we were able to achieve the task.
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/cDmz1da9TlU/0.jpg)](https://www.youtube.com/watch?v=cDmz1da9TlU)





