# v0.2 [Beta]

## Overall
* Remove parser requirement
* Implement 

## Specific
* *High Priority*: Fix preview/recording aspect ratio (from 4:3 to 16:9) and maybe size
* Record Signal Strength
* Recording Dirs (e.g. camera in DCIM)



# v0.1 [Old]
## Open Problems

* Check dataset (MMSys)
* Check orientation rate fluctuation
* Check altitude accuracy
* Check barometer

### Document
* All clocks
* Timing possibilities
* Synchronization Issues and coarse sync solutions/proposals
* Data needed for analysis/visualization
 * Number of Orientation samples per Location
 * Orientation Diff per sample ( Orient2 - Orient1) *(currently recorded in set as Sensor Duration)*
 * GPS Diff per sample ( Orient2 - Orient1) *(should be 1000)*
 * Overall Drift (**Σ**OrientDiffs - **Σ**GPSDiffs) _(should be 1000 for **N → ∞** )_
 * Average GPS accuracy (**Σ**GPSAccuracy/**N**)

### Explore
* GPS visualization
 * Adjust according to zoom, speed, density or transportation mode
    * Condence multiple neighbouring points (?)
    * Iterate
 * Fix (align to street?)
 * Project
 * When zoom in/out display more/less key-points
* Drift between high-precision OS clock and GPS time
  *  In lengthy runs
* Check network time (?)
* Thread pool

### Record
* Long-run tests
* Car, bike
* Multi-device
* Compass and Counter

-----
-----


## Fixes

### General
* Increase accuracy on video-time with Location Points map
* Add Graph with possible Location Point Switch (?)

### App
*  :zap: Check possible orientation difference in tablet / mobiles
*  :zap: Check GPS signal during recording
*  :zap: When start recording, save latest received location (?)
* Handle time recording
* Record Raw sensor data
* Consider adding multi-threading?
* Record camera/device characteristics

### Server / Processor
* ~~Fix duration of first Sensor~~
* :zap: We assume every event is recorded in order (will **NOT** be the case if/when multi-threaded)
* Handle different timing (e.g. when recording from mobile ACC is current time, MAG is uptime)
* Decide on output format

### Client
* Display alternatives in video
* ~~Calculate possible trajectories~~
* Display available switches
