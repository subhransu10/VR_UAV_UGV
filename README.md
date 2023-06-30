# Uniting UAV and UGV for Efficient Pollution Inspection
 <img src="https://user-images.githubusercontent.com/62358773/158238820-f418cc09-4227-4afc-9c31-1705dfb64f5a.png" width="5%" height="5%"> Professor Gianni Viardo Vercelli <img src="https://user-images.githubusercontent.com/62358773/158238810-c5dcb486-ba24-4b35-87de-39a54e88f36b.png" width="5%" height="5%"> Student: [Subhransu Sourav Priyadarshan](https://github.com/subhransu10)
 
 ## Introduction
The goal of the project is to inspect a natural area for pollutants risk. In order to achieve this task, we need
a UAV and a UGV. The UAV patrols the environment checking the pollutants level in the atmosphere when it
exceeds a threshold value, it sends a notification for the action that needs to be taken in order to handle the
situation and then it lands on the UGV. Both drones move autonomously in the environment and carry out the
inspection.
The UAV has a camera and a sensor equipped in order to carry out the inspection and detection process at the
same time. Then it sends a notification in case of an increase in pollutants level. The UGV has a landing pad
for the UAV.

## State of the Art
 Sudarsanan A. et al described the places where humans cannot reach, unmanned Aerial vehicles (UAV) can.Hence, environmental drones
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
+ FBX Import: With the help of this feature, we imported the .fbx files into our project. The drone (in
particular) that we used for our project is a.fbx file which is implemented by the FBX support that the
Unreal Engine provides to its users.
+ Python Scripting: We were easily able to automate our workflows with full support for the industry-standard Python scripting in the Unreal Editor through Blueprints (be it the UAV flying or UGV movement.
### World Building
+ The Unreal Editor: Unreal Engine includes the Unreal Editor, an integrated development environment
available on Linux, macOS, and Windows for content authoring and game-level development.

+ Landscape and terrain tools: We created our environment with the help of these features on Unreal
Engine. We could non-destructively edit our landscape with a layer reserved on splines and make changes
in Blueprint.
### Blueprint visual scripting system
With artist-friendly Blueprint visual scripting, we could rapidly prototype and ship interactive content
without touching a line of code. We used Blueprints to build object behaviors and interactions(such as pollutants,
fires, drone movements, etc), adjust input controls, and so much more.
### Content
+ Marketplace ecosystem: The Unreal Engine Marketplace has thousands of high-quality assets and
plugins to accelerate production and bring new functionality to your work. We were able to access new
environments, characters, animations, textures, props, sound and visual effects, music tracks, Blueprints,
middleware integration plugins, add-on tools, and full starter kits.
+ Quixel Megascans: Every Unreal Engine license comes with free access to the entire Quixel Megascans
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
+ Drone(UAV): The Drone .fbx that we used is a Phantom4 Pro. It has the ability to carry out the sensor
with a payload.
+ UGV : It is a Drivable M1126 Stryker ICV (West). It can move in any kind of difficult terrain. It has a
nozzle which can also be used to spray in the atmosphere. we use the static mesh component of the
+ Smoke: The smoke (which is caused by fire caught on wood)
+ Fire: This effect is due to the Niagara plugin on Unreal Engine. We got it from the marketplace and made
some changes according to the task.
+ Cameras: There are three cameras used in our project. There is a camera-equipped on the drone and
also a camera each to show the point of view of the drone and the UGV.
### Blueprints Used
+ Drone and its path: The Blueprint consists of three parts - path reference, flying mechanics, sensory
detection, and alert generation.
+ UGV and its path: The blueprint consists of two parts - path reference and movement.
+ Pollutants material (CO2)
## Scenario
There is a fire caused by chopped wood which is releasing harmful substances into the atmosphere(CO2) and
there is smoke due to it and the drone while patrolling, notices that the area around it is not fit for breathing
and it alerts to take some action that would control the situation.
## Future Improvements
## Results






