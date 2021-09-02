# IndoorNavigationApp
My work at Academic Sinica Open Source Software Foundry Lab(2019/5~2019/12)  
Source Code: https://github.com/OpenISDM/IndoorNavigationApp  
This page is the introduction and some easy demos of the IndoorNavigation Project  

The features of this project:  
1. Support both IOS and Android  
2. Support Multiple Language (We have built a language package that is really easy to insert new languages)  
3. The user can select the route they hope to avoid. For example, avoid the stairs, avoid the escalator or avoid the elevator.  
4. Our App can support cross the floors  
...  


The technical skills in this project  
Including but not limited to...  
1. Wu use Xamarin(C#) to built this App  
2. We use the Dijkstra to calculate the best route  
3. We use 2 kinds of beacons to indicate locations, iBeacon, and LBeacon. LBeacon is the patent of our lab. Our app can support different kinds of beacons  
4. For each important location, corner, destination..., we use a virtual point, Waypoint, to indicate it. Waypoint is based on beacon(s), if the waypoint's range is too big we use multiple beacons to indicate a waypoint.  
5. We use edges to connect Waypoints, which can help direct the user to go from one waypoint to another, and approaching the destination. The edge between Waypoints can only be cross through by walk  
![image](https://github.com/ericleee0119/IndoorNavigationApp/blob/main/image/Beacon_Waypoint_Edge_Indicate.PNG)  
6. Waypoints and Edges construct a region. There are also edges to connect regions, however, the edge between regions can be cross through by walk, stairs, elevator, escalator  
7. Multiple regions construct a graph, which is our completed map.  
![image](https://github.com/ericleee0119/IndoorNavigationApp/blob/main/image/Region_Waypoint_Edge_Indicate.PNG)  
  
8. If the user goes the wrong way, our App will recalculate the best route and give the user a new correct path 

The information of the map is built by a XML, we can scan the QR Code to download the map or download the map hat is originally saved in the APP.  
Map Information : https://drive.google.com/file/d/18xb-wp_4B2g-8sHBQdGHhvgpMtuuD5yH/view?usp=sharing  

Demo Video:  
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/mJOQX05UZIs/0.jpg)](https://www.youtube.com/watch?v=mJOQX05UZIs)


