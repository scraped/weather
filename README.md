# Weather
Weather App based on DarkSky API. Developed with Symfony.

Requirements
------------
* PHP 7.1
* Composer


Installation
------------
  
Create a Google Maps API key:

    https://developers.google.com/maps/documentation/javascript/get-api-key
    
Add your Google Maps API and Dark Sky API keys to the file:

    weather/config/services.yaml
    
    google_api_key: 'YOUR_GOOGLE_API_KEY'
    dark_sky_api_key: 'YOUR_DARK_SKY_API_KEY'
    
Run:

    composer install
    
**If you want to use the Symfony server:**    

Run server:

    php bin/console server:start
    
Use your favorite browser:

    http://127.0.0.1:8000/
    
    
**If you want to use Apache server:**        
    
Configure the project in your web server and access:

    http://{LOCALHOST}/weather/public/  

Comments
--------

The website will run faster with Apache (or Nginx) than with the embedded Symfony server.

Further work (for a real working app)
----------------------------------------

* Add unit and functional tests.

* Better and more complex exception control system.

* Add a GatewayInterface and implement a DarkSkyAPIGateway, which will be injected to WeatherService. 
This way we could easily use other weather APIs and keep a modular app. It would be also better for testing.

* Add Wrappers or Entities for transporting the weather data from the API response through the app.

* Create a separate service.
