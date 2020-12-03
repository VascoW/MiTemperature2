# reads the data of several Xiaomi Mijia LYWSD03MMC Bluetooth 4.2 Temperature Humidity sensors

With this script you can read out the values of several LYWSD03MMC sensor, e.g. with a Raspberry PI. 
The connection details of your LYWSD03MMC sensors is defined  in a config file. The script connects one after another sensor, reads out the data and publish it to a MQTT server. 
The script is a simplified version of https://github.com/JsBergbau/MiTemperature2 which I highly recommend if you want to read out one sensor or want to use the result other than in MQTT. 

While I removed certain parts of the code I added direct connection to MQTT (via Paho MQTT) and the opportunity to request several sensors with the same script/cron job. 

* Caveat: requesting data from this sensor is rather slow. It usually takes around one minute per sensor. Therefore the numbers of sensor is limited based on the frequenzy you want to use (I use 3 sensors every 5 minutes which works well). 

For installation and usage it's fairly similar to https://github.com/JsBergbau/MiTemperature2 

Eventually one day I will find time to explain it here since I removed some dependencies and added others :) 
