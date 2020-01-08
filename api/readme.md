## Routes ##
* Get list of all sensors: http://localhost:3000/api/sensors
* Get list of all sensors, min day and max day: http://localhost:3000/api/info
* Get Sensor in range: http://localhost:3000/api?sensor=123&min=123&max=321
* Get Sensor in range (force accurate data): http://localhost:3000/api/accurate?sensor=123&min=123&max=321
* Get Sensor in range (force average hourly data): http://localhost:3000/api/average/day?sensor=123&min=123&max=321
* Get Sensor in range (force average daily data): http://localhost:3000/api/average/hour?sensor=123&min=123&max=321
* Get all average data: http://localhost:3000/api
* Get all average data for one sensor: http://localhost:3000/api?sensor=123

## Data ##
When requesting data without forcing a specific type (average) the API will choose the best.
When the time range is smaller than 5 hours, it will send the full data. For a time range smaller than a week you will get a hourly average. Everything else is a daily average.