# DroneSimulator

The main goal for this project is to try find good solution of small drone, flying inside indoor building without getting hit and crash.
The project fully autonomous 2d drone simulator, this simulator is trying to be realistic as much as it can, with lidar sensors,gyroscope sensor ,optical flow sensor and speed sensor.
We add a little bit noise to each sample to make it more realistic approach.
Basic API with real-time info and also manual controlling.
We also implemented kind of area mapping when the drone fly.
* This project was written in Java.
  
  ![](https://www.extremefliers.com/wp-content/uploads/2021/12/how-to-program-a-drone11.jpeg)                       
  
## Getting Started

When all files located inside eclipse or any other explorer we have the Maps folder which contains couple of maps with route and obstacles.
- Inside "SimulationWindow" in main we have map object with the path to any map you want to test.
- Inside "Drone" we have path to our image represents the drone itself.
After setting this up it is ready to launch.

## Sensors
- Lidar - check the distance between his spot forward and return the distance if hit, if not return 300 as max sample enabled.
In our project we set 3 lidars - one in front, second 90 degrees, third -90 degrees.
- Gyroscpoe - check the rotation of the drone. (0-360)
- Optical flow - check his location on map.
- Speed - max speed is 2m per second.

- ![](https://cdn.sick.com/media/895/0/70/770/IM0090770.png)
- ![](https://www.bhphotovideo.com/images/images500x500/hubsan_zino000_06_gyroscope_module_for_h117s_1496876.jpg)
- ![](https://i.stack.imgur.com/S1APo.jpg)
- ![](https://cdn-global-hk.hobbyking.com/media/catalog/product/cache/4/image/660x415/17f82f742ffe127f42dca9de82fb58b1/legacy/catalog/110366.jpg)


## Symbols 
- Yellow mark - mapped area.
- Black circle - his purpose to get some idea from where drone came and simply make some route that his passed.(for navigation)
- Red points - represents the wall point.
- Blue line - his whole route.

## API description
Really simple API with few buttons -
Start/pause button, speed up/down, spin -+30/-+45/-+60/90/180.
- Toggle Map - allows you to hide the real map, entering to "real time" vision.
- Toggle AI - enable/disable AI.

![](https://res.cloudinary.com/crunchbase-production/image/upload/c_lpad,f_auto,q_auto:eco,dpr_1/lywumalmsvcgb6yrtbvo)

## Map rules
If you wish to add custom map it has to be black/white pixels- black is wall/obstacle, white is safe pass.

## V2 update
- Added return home bottom, by clicking it drone will return to starting point.
- Directed Graph feature added. (JGrapht library required)
- 
![image](https://m.media-amazon.com/images/I/61OQEmuM6hL._AC_SY355_.jpg)

## Known bugs
- API might be in different place depends on the map.
- Sometimes drone might crash(hit the black pixels) specially in difficult obstacles.
- Sometimes may be indifferent parameters which causing some pixels override - solution is to re-run project.

## Images
![](https://i.imgur.com/lweL2Fp.png)
![](https://github.com/ahmadabed1/DroneSimulator/blob/main/Images/Image3.png?raw=true)

![graphexample](https://user-images.githubusercontent.com/28596354/60256218-cc095680-98d9-11e9-8ab4-70c00e863df8.png)
