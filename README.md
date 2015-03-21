# Smart-Weather-Lamp
A SmartThings app for a color changing smart weather lamps that changes color with the weather. 

If you're like me, you've had your share of weather this year.  I decided to use SmartThings to better visualize the weather - and to know whether I need an umbrella, a coat, a snow shovel, some tissues (for high pollen) or sandals and shorts when I head out the door. 

Enter the color changing smart weather lamp app.  It uses a motion sensor and one or more Phillips Hue or LifX LED bulbs to visually display the weather forecast. Use your favorite lamp fixture. 
Here is a quick video that shows how it works. http://youtu.be/ycUlqro_QMo   The video doesn’t sufficiently capture the cool and vivid colors created by the Hue bulb, but you get the idea.   

Weather Lamp Colors

     •	Blinking Red  -- A weather watch, warning, or advisory is in effect in your area.  
   
     •	Purple  -- Rain: It’s raining outside. Triggers when there is greater than 15% chance of rain in this or the next hour
     
     •	Blue  --  Cold: It’s freezing outside
     
     •	Pink  -- Snow:  Snow is forecast for the day
     
     •	Orange  -- Hot:  It’s hot outside -- above 80F
     
     •	Green  --  Sneeze: Pollen is in the air - above 7 (pollen requires integration with IFTTT that sets a virtual switch in ST)
     
     •	White  -- All clear
   
To get accurate weather information it, for example, uses the specific latitude and longitude from your SmartThings Hub to take advantage of weather micro-targeting API at forecast.io that powers the App DarkSky.  They believe they can predict when it will rain — down to the minute — at your exact location.  To use the forecast.io API for your weather forecast, visit https://developer.forecast.io/register, register to get an API key, and insert it on line 129 of the groovy script.

If there is a weather emergency, the app can send you a text message to warn you.  

If you are an allergy sufferer and want the lamp to turn green when there is a high pollen count outside, then there is a bit of a hack.  Create a virtual switch in SmartThings: http://thinkmakelab.com/2014/06/11/how-to-create-a-virtual-switch-in-smartthings/   Then create an account at IFTTT.com if you don’t already have one, add a SmartThings channel to your account, and then add this recipe and link it to the virtual switch you created in ST.  https://ifttt.com/recipes/264981-if-pollen-count-gets-high-turn-smartthings-switch-on-works-w-color-changing-smart-weather-lamp  Then select the Virtual Switch in the settings of the SmartLantern App.

Here’s to good weather!

