# Radar
Detects objects and estimate their parameters from a distance. A FMCW (Frequency Modulated Continuous Wave) radar offers relatively small form factor with low power and low cost.
Applications of FMCW Radar
    * BSD: blind spot detection
    * RCW: rear collision detection
    * ACC: Adaptive cruice control
    * D&C: object detection and classification (Pedestrians, Bicycle, Cars/Vehicles, etc)
FMCW can measure,
    * Range(distance)
    * Relative velocity
    * heading angle
    * RCS (Used for D&C)
















# All sensors in a nutshell

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