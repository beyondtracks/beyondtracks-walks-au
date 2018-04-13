# MOVED to https://gitlab.com/beyondtracks/beyondtracks-walks

These are the source files defining walks on [www.beyondtracks.com](https://www.beyondtracks.com).

They were created in [JOSM](https://josm.openstreetmap.de/) partially derived from OpenStreetMap data. Around 95% of the geometries were copied from OpenStreetMap data the other was from personal GPS track recordings. In some cases, names were also from OpenStreetMap but mostly they are self sourced.

New walks Australia wide are welcome for contribution, but I reserve editorial decisions on what's included. 

# License
Contains information from OpenStreetMap copyright OpenStreetMap contributors, which is made available here under the [Open Database License (ODbL)](http://opendatacommons.org/licenses/odbl/1.0/).

This repository contains a derivative database of OpenStreetMap and as such is licensed under the [ODBL](http://opendatacommons.org/licenses/odbl/1.0/).

When using this data in other works, please provide attribution. For example: "Contains data from [BeyondTracks.com](https://www.beyondtracks.com)."

# Schema
## Ways
* **name** Either a commonly known name for the walk or start/end points including a notable waypoint if it's necessary to avoid ambiguity.
* **park** Name of the CAPAD protected area which most of the walk falls in. Walks which span multiple parks aren't well supported so for the time being only one can be listed. In the future this may be removed by an automated process.
* **photo** ID of a photo which best represents the walk. Currently it's a Flickr photo ID within andrewharvey4 user account. In the future this will support any photo from Flickr.
* **style** `oneway` | `return` | `loop` Value depending on if the walk starts and ends at the same point or not and if you need to backtrack the route or not.
* **role** `primary` | `sidetrack` | `altroute` | `transit_connection` A single walk can have multiple ways, one must be the `primary` way but you can also have sidetracks, alternative routes and ways for getting to the start of the walk from a nearby public transit stop.
* **transport** `carshuffle` | `car` | `foot` | `train` | `bus` | `ferry` | `taxi` | `chairlift` What methods of transport are viable ways of getting to/from the start/end of the walk. Multiple options are separated by a `;`, where multiple options are required together use a `+`. eg. `car;train+bus` means you can either take a car or take a train and bus. Car shuffle is when the end of the walk is away from the start and you need to shuffle multiple cars to complete the trip.

## Nodes
* **warn** `hazard` | 'information` | `navigational` | `rivercrossing` Used to flag a warning
* **note** Description of the warning
