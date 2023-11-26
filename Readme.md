# Self drving car sensors

Collection of theory and code about sensors used in self drving cars. 

* [x] Radar
* [x] Camera
* [x] Lidar
* [ ] GPS
* [ ] IMU
* [ ] Sensor system calibration  


## Radar
Detects objects and estimate their parameters from a distance. A FMCW (Frequency Modulated Continuous Wave) radar offers relatively small form factor with low power and low cost.

#### [Radar Theory](Radar/Readme.md)

#### Applications of FMCW Radar
* BSD: blind spot detection
* RCW: rear collision detection
* ACC: Adaptive cruice control
* OD&C: object detection and classification (Pedestrians, Bicycle, Cars/Vehicles, etc)
#### FMCW radar can measure
  * Range(distance)
  * Relative velocity
      * Doppler effect
      * Frequency modulation
      * Beat frequency 
  * Heading angle/direcction (Azimuth & Elevation)
  * RCS (Used for OD&C)

## Camera 

#### [Camera Theory](Camera/Documents/Camera%20Calibration.pdf)

#### Camera calibration
  * [Camera calibration Theory](Camera/Documents/Camera%20Calibration.pdf)
  * [Calibration code](Camera/src/CameraCalibration.py)
  * [How to use it and results](Camera/README.md)


## Lidar

#### [Lidar Theory](Lidar/readme.md)


## All sensors in a nutshell
[source](https://github.com/fanweng/Udacity-Sensor-Fusion-Nanodegree/blob/main/README.md)

|  Criteria  |  Lidar  |  Radar  |  Camera  |
|------------|---------|---------|----------|
| **Range**      | Meters to 200m | Meters to 200m | Only stereo camera setup can measure distance up to 80m |
| **Spatial Resolution** | High, 0.1 degree due to short wavelength laser | Cannot resolve small features | Defined by optics, pixel size of image and its signal-to-noise ratio |
| **Robustness in Darkness** | Excellent, due to active | Excellent, due to active | Reduced |
| **Robustness in Rain, Snow, Fog** | Limited, due to optical | Best | Limited, due to optical |
| **Classification of Objects** | Some level of classification by 3D point clouds | Not too much classification | Excellent at classification |
| **Perceiving 2D Structures** | N/A | N/A | The only sensor that is able to interpret traffic signs, lane markings, traffic lights |
| **Measure Speed** | Approximate speed by using successive distance measurement | Measure velocity by exploiting the Doppler frequency shift | Can only measure time to collision by observing the displacement of objects on the image plane |
| **System Cost** | More expensive | Compact and affordable | Compact and affordable |
| **Package Size** | Hard to integrate | Easily integrated | Easily integrated for mono cameras, but stereo camera setup is bulky |
| **Computational Requirements** | Little | Little | Significant |