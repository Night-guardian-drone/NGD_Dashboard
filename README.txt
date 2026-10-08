Night Guardian Drone — Updated Ground Control Dashboard

This version combines the new route-planning map with the older dashboard information shown in the supplied reference:
- Latitude
- Longitude
- Altitude
- Climb rate
- Ground speed
- Heading
- Satellites
- GPS fix
- Arm status
- Flight mode
- Ultrasonic radar
- Radar distance
- Radar angle (90°)
- Sensor status
- System event log
- Separate APM and Radar connections
- Disconnect APM
- Disconnect Radar
- Disconnect All
- Route planning / waypoints
- Start/Clear route
- Obstacle warning and RTL status display

Serial:
- Arduino HC-SR04 radar: 9600 baud
- APM telemetry: 115200 baud

Note: the RTL feature in this dashboard displays the RTL state and stops the planned route. It does not send an actual autonomous RTL command to the APM.


FIX:
The previous build had a JavaScript syntax error in the map click handler. That prevented Leaflet from initializing, which is why the map area appeared blank. This build fixes that error.

RADAR UPDATE:
- The HC-SR04 is fixed at 90 degrees, so the target dot now stays on the centre radar axis.
- Distance changes move the dot inward/outward on that axis instead of sideways.
- Added a separate large LIVE DISTANCE numeric box in cm.

RADAR VISUAL SCALE UPDATE:
- The radar dot now uses a 0–200 cm visual range so common obstacle distances move much more noticeably.
- The displayed distance number remains the actual HC-SR04 measurement.
- The dot remains on the fixed 90° centre axis.
