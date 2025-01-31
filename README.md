# Building a Magic Mirror with Raspberry Pi, Docker, WS2812B LED Strip & APIs 🪞💡

I recently turned an old monitor into a **Magic Mirror**—an interactive display that shows weather, time, news, and calendar events. Instead of using a Raspberry Pi Zero W, which couldn’t handle the resource-heavy **MagicMirror²**, I repurposed a spare **Raspberry Pi 3** to act as the server.

## Why Raspberry Pi Zero W & MagicMirror²?

**MagicMirror²** displays modules like weather, time, news, and calendar events. However, the Pi Zero W struggled to run the app due to its limited processing power. Therefore, I used the **Pi 3** to handle the backend processing and fetching data from external APIs.

## The Two-Pi Setup

1. **Server (Pi 3)**:  
   The Pi 3 runs **MagicMirror²** and fetches live data from external APIs like OpenWeatherMap (weather), NewsAPI (news), and Google Calendar API (events).

2. **Client (Pi Zero W)**:  
   The Pi Zero W handles rendering, offloading the processing to the Pi 3 via HTTP communication.

3. **Docker**:  
   MagicMirror² runs inside a **Docker container** on the Pi 3. Docker isolates the app from other services, ensuring smoother operation and easier management.

## API Integration

To keep the Magic Mirror updated with real-time data, I integrated the following APIs:

- **Weather**: OpenWeatherMap API
- **News**: NewsAPI
- **Calendar**: Google Calendar API

These APIs update the Magic Mirror with live information.

## Adding a WS2812B LED Strip

I integrated a **WS2812B LED strip** controlled by an **ESP32** running **WLED**. The ESP32 communicates with the Pi via **MQTT** to sync the LED strip’s color and lighting effects based on time, weather, and calendar events.

## Why Docker?

Docker simplifies deployment and ensures that **MagicMirror²** runs independently of other services on the Pi 3. It isolates the application, making it easier to manage, update, and scale.

## MagicMirror² Software: What’s Inside

**MagicMirror²** displays:

- **Weather**: Live updates from OpenWeatherMap
- **Time & Calendar**: Time and events fetched from Google Calendar
- **News Feeds**: Headlines from NewsAPI

The software is highly customizable with a variety of community-developed modules, allowing you to tailor it to your needs.

## Key Takeaways

- **Docker** made deployment simpler and kept **MagicMirror²** isolated from other services on the Pi 3.
- Using a **Pi 3 (server)** and **Pi Zero W (client)** improved performance and power efficiency.
- The **WS2812B LED strip** adds dynamic lighting effects synced with the Magic Mirror’s data.
- **APIs** keep the Magic Mirror updated with weather, news, and calendar events.

This project was a great opportunity to reuse old hardware, dive deeper into **Docker**, and experiment with **IoT**. If you have spare Raspberry Pis lying around, I highly recommend giving this a try!

Feel free to reach out if you have any questions or want to share your own setup!

## Technologies Used

- **Raspberry Pi 3** (Server)
- **Raspberry Pi Zero W** (Client)
- **MagicMirror²**
- **Node.js**
- **CSS**
- **Docker**
- **OpenWeatherMap API**
- **NewsAPI**
- **Google Calendar API**
- **WS2812B LED Strip**
- **ESP32 & WLED**
- **MQTT**


