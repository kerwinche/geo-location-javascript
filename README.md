# geo-location-javascript
Automatically exported from code.google.com/p/geo-location-javascript

Location based mobile websites
Goal is to provide a usable geo location framework for mobile websites/widget applications. It wraps the underlying platform specific implementation through a simple JavaScriptAPI that is aligned to the W3 Geolocation API Specification..

//determine if the handset has client side geo location capabilities
if(geo_position_js.init()){
   geo_position_js.getCurrentPosition(success_callback,error_callback);
}
else{
   alert("Functionality not available");
}
Usage Scenario
The framework provides two key methods, it determines if the handset has client side geo location capabilities and one method to retrieve the location (of course only after a request for permission). So a mobile web site that provides location based services can first determine if the client has client side geo capabilites and ask him to assist him in finding his location. If no geo capabilities are given or they are disabled the site can fallback on a manual location input method and use a geodata database/service to map the input to a pair of latitude/longitude coordinates.

Supported platforms
iOS
Android
Blackberry OS
Browsers with Google Gears support (Android, Windows Mobile)
Nokia Web Run-Time (Nokia N97,...)
webOS Application Platform (Palm Pre)
Torch Mobile Iris Browser
Mozilla Geode
Details...

Simulation
To assist engineers in the development phase it provides a simple mechanism to simulate users locations and movements without being there in the real world.

Sample Web Pages
Very simple page that provides a status alert box
Show the users location in an embedded google map(v3), requires advanced browsers
Simulates a moving user in an embedded google map(v3), requires advanced browsers

Sample Apps
Nokia Web Run-Time Sample - download and transfer to the device


The simulator helps in the development phase of projects. 
It lets you simulate a user on a certain location or a moving user without being at those places in the real world.

Usage
First you need to include the simulator library

<script src="js/geo_position_js_simulator.js" type="text/javascript" charset="utf-8"></script>

then create an array whose elements are simple hashs with latitude/longitude and the duration of the stay in seconds. Example: if you have 2 those entries, the second entry gets activated as the current location after the duration of the first one has expired.

locations=new Array();
locations.push({ coords:{latitude:41.399856290690956,longitude:2.1961069107055664},duration:5000 });
locations.push({ coords:{latitude:41.400634242252046,longitude:2.1971797943115234},duration:5000 });
locations.push({ coords:{latitude:41.40124586762545,longitude:2.197995185852051},duration:5000 });      
Lastly initialize the simulator and do that before you initialize the toolkit.

geo_position_js_simulator.init(locations);
Check it out in action:

Simulates a moving user in an embedded google map(v3), requires advanced browsers
