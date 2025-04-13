# Assignment 9: Domain Model for Weather Tracking System

## Domain Model Description

The domain model for the Weather Tracking System captures the core entities and their interactions within the application. It reflects how real-world components—such as users, sensors, and weather data—are structured and behave within the system. This model provides a conceptual foundation for both database design and object-oriented programming structures.

### Key Entities:
- **UserAccount**: Represents users registered in the system, including standard and administrative roles.
- **Location**: Stores geographical data for weather tracking, customized per user.
- **Sensor**: Embedded within weather stations to collect environmental data like temperature and humidity.
- **WeatherStation**: Collects and transmits sensor data; monitored for health and uptime.
- **WeatherReport**: Compiled and validated summaries of collected weather data.
- **ForecastRequest**: Captures user or system-initiated forecast generation requests.
- **Alert**: Issued in case of severe weather conditions; linked directly to reports.

Each entity encapsulates relevant attributes and methods that define its state and behavior. Relationships are modeled to express cardinality and direction—for example, a weather station **has many** sensors, and a user **has many** forecast requests.

By structuring the domain model in this way, the system ensures:
- **Encapsulation** of data and behavior within logical objects.
- **Traceability** to functional requirements and user stories.
- **Scalability** through reusable and modular entities.

This model forms the basis for system architecture, guiding both the implementation and expansion of the Weather Tracking System.


## 1. Domain Model Table

| **Entity**        | **Attributes**                                                                 | **Methods**                                                     | **Relationships**                                                | **Business Rules**                                                                 |
|-------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `UserAccount`     | userID, name, email, password, role                                            | register(), login(), updateProfile(), deleteAccount()            | One-to-Many with `Location`, `ForecastRequest`                   | Must verify email before accessing weather services.             |
| `Location`        | locationID, name, latitude, longitude, userID                                  | saveLocation(), updateLocation(), deleteLocation()               | Many-to-One with `UserAccount`; One-to-Many with `WeatherReport` | Coordinates must be within valid geographic ranges.              |
| `Sensor`          | sensorID, type, status, lastReading, stationID                                 | readData(), calibrate(), reportError()                           | Many-to-One with `WeatherStation`                                | Only active sensors can transmit data.                           |
| `WeatherStation`  | stationID, location, status                                                     | initialize(), sendData(), performCheck()                         | One-to-Many with `Sensor`                                        | Must send health status every 10 minutes.                        |
| `WeatherReport`   | reportID, timestamp, temperature, humidity, windSpeed, locationID              | generateReport(), validateReport(), archiveReport()              | Many-to-One with `Location`                                      | Reports must be generated at fixed hourly intervals.             |
| `ForecastRequest` | requestID, userID, locationID, requestTime, forecastType                       | submitRequest(), processRequest(), returnForecast()              | Many-to-One with `UserAccount` and `Location`                    | Only authenticated users can submit forecast requests.           |
| `Alert`           | alertID, type, severity, issuedTime, expiryTime, reportID                      | triggerAlert(), cancelAlert(), notifyUsers()                     | One-to-One with `WeatherReport`                                  | Alerts must be sent for severity ≥ 3 on a 5-point scale.         |

---

