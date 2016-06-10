These are the source files defining walks on [www.beyondtracks.com](https://www.beyondtracks.com).

They were created in [JOSM](https://josm.openstreetmap.de/) partially derived from OpenStreetMap data. Around 95% of the geometries were copied from OpenStreetMap data the other was from personal GPS track recordings. In some cases, names were also from OpenStreetMap but mostly they are self sourced.

New walks Australia wide are welcome for contribution, but I reserve editorial decisions on what's included. 

# License
This repository is licensed under the ODBL as they are derived from OSM data.

# Schema
* **name** Either a commonly known name for the walk or start/end points including a notable waypoint if it's necessary to avoid ambiguity.
* **park** Park name of the CAPAD protected area which most of the walk falls in. Walks which span multiple parks aren't well supported so for the time being only one can be listed. In the future this may be removed by an automated process.
* **photo** ID of a photo which best represents the walk. Currently it's a Flicker photo ID within my user account.
* **style** `oneway` | `return` | `loop` Value depending on if the walk starts and ends at the same point or not and if you need to backtrack the route or not.
* **role** `primary` | `sidetrack` | `altroute` | `transit_connection` A single walk can have multiple ways, one must be the `primary` way but you can also have sidetracks, alternative routes and ways for getting to the start of the walk from a nearby public transit stop.
* **transport** `carshuffle` | `car` | `walk` | `train` | `bus` | `ferry` What methods of transport are viable ways of getting to/from the start/end of the walk. Multiple options are separated by a `;`, where multiple options are required together use a `+`. eg. `car;train+bus` means you can either take a car or take a train and bus. Car shuffle is when the end of the walk is away from the start and you need to shuffle multiple cars to complete the trip.
