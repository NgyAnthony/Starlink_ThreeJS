![Starlink Satellites - ThreeJS Visualization](https://i.imgur.com/QwQAD16.png)

# Starlink Satellites - A ThreeJS Visualization powered by Python

#### [Website](https://starlink-tracker-20c00.web.app "Website") - [API](https://dashboard.heroku.com/apps/starlink-tracker "API") - [TLE API (CelesTrak)](https://www.celestrak.com/NORAD/elements/starlink.txt "TLE API")
## Development

### Backend
Related to : [Python repository](https://github.com/NgyAnthony/skyfield_starlink "Python repository")

With the CelesTrak data as a source, I used the Skyfield library from Python to decode TLE (Two Line Element set, used to describe the position of a Satellite among other things) and extract only the latitude, longitude and elevation of the satellite.

As a result, this script is able to output a single array with all the coordinates of the satellites. Using Flask, the live data from the TLE API is provided to the front-end as an API to be consumed by ThreeJS

### Front-end
A simple WebGL/ThreeJS globe from Google DAT enabled me to easily place the satellites at scale.

## References
##### **Thanks to:**
##### [orbital_objects (Alex Rasmussen)](https://github.com/alexras/orbital_objects/ " orbital_objects (Alex Rasmussen)") - [WebGL Globe (Google Data Arts Team)](https://github.com/dataarts/webgl-globe "WebGL Globe (Google Data Arts Team)")
