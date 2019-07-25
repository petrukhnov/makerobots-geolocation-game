

# Structures

Structure contain levels, that look like fallout game.

Each deeper/higher level will cost more.


## levels

Max width is based on max height (sum of levels). E.g. if there are 3 levels above ground and 5 levels under ground, max width (horizontal rooms) is 8 at every level.
Cost for each next +1 or -1 level:

Base structure: 1/1 (knowledge/quanta). Provide 1 above ground and 1 underground room.

* 1 -> 1/1
* 2 -> 1/2
* 3 -? 1/5
* 4 -> 1/10
* 5 -> 1/30
* 6 -> 1/50
* 7 -> 1/100
* 8 -> 1/250
* 9 -> 1/500
* 10 -> 5/1000
* 11 -> 5/2K
* ...
* 19 -> 5/9K
* 20 -> 10/10K
* 21 -> 10/20K
* ...
* 30 -> 10/100K
* ...
* 40 -> 50/1M
* ...
* 50 -> 100/10M
* ...
* 60 -> 500/100M
* ...
* 70 -> 1K/1G
* ...
* 80 -> 5K/10G
* ...
* 90 -> 10K/100G
* ...
* 100 -> 50K/1T
* ...


## Distance

Min distance between structure is 1km OR structure width*0.1km (whichever is bigger.) 

E.g. structures  with width 3, will not allow placing buildings closer than 1 km.

E.g. structures  with width 13, will not allow placing buildings closer than 1.3 km. 

Also nearby structures may prevent from adding more rooms on same level.

# Facilities

Facility is construction inside structure. Facility occupy one room. When destroyed, it don't give back anything.

* Knowledge collectors
  * Automatic knowledge collector. 10 char collection. +10% infinite upgrades. 
* Knowledge refineries
* Servers (store knowledge)
* Quanta collectors
  * Basic
  * Quarry
  * Pumpjack
  * Infinite
* Quanta refineries. +10% speed infinite upgrades
  * 5 for raw -> pure (0.1/0.3/0.5/0.7/1.0x)
  * 10 for crude -> raw 
  * 30 for essence -> crude
* Quanta storage (storage get)
  * Pure (don't need storage, available always)
  * Raw (100 rooms should store 10K) One room store 100. Infinite +10% capacity upgrade. 
  * Crude (1K rooms should store 10M) One room store 1K. Infinite +10% capacity upgrade. 
  * Essence (10K rooms should store 1T). One room store 1G. Infinite +10% capacity upgrade.
* Pure quanta transmitter. Transmit pure quanta to team storage. From that network.
* Quanta scanners (automatically scan for new resources once a day). Range 1km radius. Infinite range upgrade +10%
  * vein
  * lake
  * infinite
* Research lab
* Antenna. Enabled if top level of the building. Used to send commands to stars.+
* Launch pad. (enabled if it open to sky and 2 rooms left/righ is also open to sky.)
* Rocket factory. Enabled if same level as launch pad.
* Space Agency Hub. When 2 teams build hubs in structures that are less than 1km from each other, they may use antennas of other team.
* Rocket survey team room. Give 1 knowledge for each own/space agency rocket launched in 1km radius. Infinite radius upgrade +10%.
* Rocket spy team room. Give 1 knowledge for each enemy rocket launched in 1km radius. Infinite radius upgrade +10%. 
* Structure connector. Allow connect other structure, that have free connector at same level.

# Connection pipes.

Distance is 5km. 

Infinite distance upgrades +10% 

Default max time to connect 2 structures is 1hour. 

Infinite time upgrade +10%.

# Optimized resource calculation

Tick every hour. Or when player connect/disconnect new structure. Or create/destroy facility.

1. List all connected structures.
1. Calculate resource collection from all facilities.
1. Calculate resource refinements from all facilities.
1. Subtract resources spend for research.
1. Subtract resources spend for production.
1. Transfer pure resources to team.
1. Check if any rockets should be launched.