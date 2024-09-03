# plantY
first year engineering ideathon project. PlantY is a plant health device equipped with multiple sensors.
The Smart Plant Project uses an ESP8266 microcontroller to monitor environmental conditions such as temperature, humidity, and soil moisture for a plant. The data is sent to the Blynk app, allowing users to monitor and manage their plant's environment remotely. 

the code was writtin on arduino IDE.

# Features
- monitors temperature and humidity with a DHT sensor
- measures soil moisture levels using a soil moisture sensor
- sends real time data to Blynk app

# Components
- ESP8266 WiFi Module
- DHT11 Temperature and Humidity Sensor
- Soil Moisture Sensor

# Installation

## Hardware Setup
- Connect the DHT sensor to GPIO pin D2 (GPIO4) of the ESP8266.
- Connect the soil moisture sensor to the analog pin A0.

## Software Setup
- Ensure you have the Arduino IDE installed. Download it from the Arduino website.
- Install the following libraries through the Arduino Library Manager:
- Blynk Library: Search for "Blynk" and install it.
- DHT Sensor Library: Search for "DHT sensor library" and install it.

## Blynk Setup
- Create a Blynk account and set up a new project in the Blynk app.
- Copy the Auth Token provided by Blynk and replace BLYNK_AUTH_TOKEN in the code with your token.
- Add widgets to your Blynk project and assign them to virtual pins (V0, V1, V2) as used in the code.

## Upload Code
- On Arduino IDE select the appropriate board and port in tools and upload sketch.

# Setup Function
- Initializes serial communication.
- Sets up the DHT sensor and connects to Blynk using the provided Auth Token and WiFi credentials.

# Loop Function
- Reads temperature and humidity from the DHT sensor.
- Logs the data to the Serial Monitor.
- Sends the temperature and humidity readings to Blynk virtual pins V0 and V1.
- Reads and sends soil moisture data to Blynk virtual pin V2.


