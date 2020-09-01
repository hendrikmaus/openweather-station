# 📡 OpenWeather Station

> An open source weather station that uses the [OpenWeather Station API 3.0](https://openweathermap.org/stations) for a backend.

## 🔬 Features

- Measurements
  - Temperature
  - Humidty
  - Atmospheric pressure
  - Wind speed
  - Wind direction
  - Rain amount
- Solar Powered
- Connectivity
  - WiFi
  - SIM card
  - LoRa

Please also find the unofficial [companion app](https://github.com/hendrikmaus/openweather-station-companion-app) to manage your station and quickly retrieve its measurements on the go.

## 🚜 Bill of Materials (BOM)

> Links are _non_-affiliate and reflect what was available in August 2020 in Europe.

- Power
  - [5w solar panel](https://www.amazon.de/dp/B00XHREE50?psc=1)
  - [DC-DC converter](https://www.amazon.de/gp/product/B07Q9PSFG1)
  - [TP4056 charge controller](https://www.amazon.de/gp/product/B077XW1XBJ)
  - [Li-Ion cell (e.g. 18650 type)](https://de.aliexpress.com/item/32810182330.html)
  - [18650 mount](https://de.aliexpress.com/item/32821011990.html)
- Controller
  - [ESP32](https://www.amazon.de/gp/product/B074RGW2VQ)<sup>1</sup>
- Connectivity (one of)
  - [LoRa module](https://www.amazon.de/MakerHawk-%C3%9Cbertragungsmodul-Spread-Spektrum-Kommunikation-Gemessener-Anti-Interferenz-Leistung/dp/B07GQQ5Q4W)<sup>2</sup>
  - [SIM800L](https://www.amazon.de/DollaTek-GSM-Modul-Micro-SIM-Karte-serielle-Schnittstelle/dp/B081JYDYGH)<sup>3</sup>
- Sensors
  - [BME280](https://www.amazon.de/gp/product/B07KY8WY4M)
  - [WH-SP-WS01 Anemometer](https://de.aliexpress.com/item/4000347448903.html)
  - [WH-SP-RG Rain gauge](https://de.aliexpress.com/item/4000407106038.html)
  - [MS-WH-SP-WD Wind direction](https://de.aliexpress.com/item/1000001854801.html)<sup>4</sup>
- Misc
  - Aluminum profiles for framing
  - Plastic case
  - Stevenson screen
  - A post (do not mount to a building<sup>5</sup>)
  - Wires
  - Resistors
  - Capacitors

_<sup>1</sup> Depending on your chosen type of connectivity, you may find readily available ESP32 boards with, for example, a SIM800L on-board. To optimize for low-power operation, you should consider to not use a development board, but a bare ESP32 chip. However, a development board should be fine, even in countries with little sun in winter, since the MCU will be in deep sleep most of the time._

_<sup>2</sup> If you decide for LoRa, please choose the appropriate frquency band for your location._

_<sup>3</sup> Choosing the SIM800L requires you to also purchase a SIM card with some sort of data plan. I went with ThingsMobile for testing._

_<sup>4</sup> I did not include the wind direction measurement in my build as of 2020/09_

_<sup>5</sup> Mounting the station to a building would invalidate multiple sensor readings, e.g. heat radiates from a wall, the rain gauge might be partially shielded, the anemometer might be blocked but wind still present etc._

> You can decide to either extend or reduce the sensors of your station; please have a look at what the [API](https://openweathermap.org/stations#measurement) supports.
