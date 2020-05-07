# The Weather is Cool
This is a project I made for my Internet of Things class in Spring 2020.

### Components
- Raspberry Pi 3
- 4 LEDs, red, green, blue, yellow
- Sparkfun motor driver
- Dagu DC motor
- Flag made out of skewers and fabric
- [OpenWeatherMap API](https://openweathermap.org/current)
### How it Works
When the user runs `weather.py` they will be prompted to input the city and state on the command line and the program will call the API and actuate the wind speed on the motor and the wind directions on the LED. The motor speed is between 0 and 1, but the API returns meters per second so I had to convert it into a number between 0 and 1. I converted the wind speed to mph and then divided it by 240, I used 240 because that is the highest the wind speed can be. The direction is displayed on the LEDs. The API returns the direction in degrees, so I calculated the direction by giving each direction 45 degrees on the compass. I did this because there are some directions I cannot show, such as east northeast.
- North is red
- East is blue
- South is yellow
- West is green

Intermediate directions can also be shown by lighting up both LEDs, for example, northwest can be shown by lighting up the red and green LED. View the pictures and the video in the repo to see it in action!
### Features I would like to add
- A web interface where the user can type in a city or pick from a list of selected of cities
- On the web interface, give the user some information about the city, such as population, current weather, historical facts about the city
- Actuate more weather information, such as temperature, pressure, humdity
- Add international cities
