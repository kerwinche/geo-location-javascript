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
