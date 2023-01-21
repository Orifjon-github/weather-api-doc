# **All Cities**

  Returns json data about all cities Uzbekistan with longitude and latitude. (paginate(10))

  -------------------------

 **URL**

  `http:127.0.01:8000/api/cities/`

 **Method:**

  `GET`

 **Success Response:**

```json
{
    "success": true,
    "code": 200,
    "message": "OK",
    "data": [
        {
            "id": 1,
            "name": "Tashkent",
            "longitude": "69.2667",
            "latitude": "41.3000"
        }, ... 
    ] 
}
```

  **Error Response:**

```json
{
    "success": false, 
    "code": 404, 
    "message": "Not Found"
}
```

# **Get city by ID**

  Returns json data single city information

  -----

 **URL**

  `http:127.0.01:8000/api/cities/1`

 **Method:**

  `GET`

 **Success Response:**

```json
{
    "success": true,
    "code": 200,
    "message": "OK",
    "data": {
        "id": 1,
        "name": "Tashkent",
        "longitude": "69.2667",
        "latitude": "41.3000"
    }
}
```

 
 **Error Response:**

```json
{
    "success": false, 
    "code": 404, 
    "message": "Not Found"
}
```

# **Create City**

  Returns json data single city information

  -----

 **URL**

  `http:127.0.01:8000/api/cities`

 **Method:**

  `POST`

  **Data Params**

  **Note:** All parameters is required and Name is Unique

  ```json
{
    "name": "Test",
    "latitude": "121212",
    "longitude": "12121"
}
  ```

 **Success Response:**

```json
{
    "success": true,
    "code": 201,
    "message": "City Created Successfully",
}
```

 
 **Error Response:**

```json
{
    "success": false,
    "code": 405,
    "message": "Validation Error: Name, Longitude and Latitude required! Name field is Unique"
}
```

# **Get All Weather Information**

  Returns json data about all cities weather informations hourly. paginate(10)

  -----

 **URL**

  `http://127.0.0.1:8000/api/weather/all`

 **Method:**

  `GET`

 **Success Response:**

```json
{
    "success": true,
    "code": 201,
    "message": "City Created Successfully",
    "data": [
        {
            "id": 1,
            "city": "Tashkent",
            "time": "2023-01-21 15:00:02",
            "weather_name": "Clouds",
            "temperature": 2.81,
            "pressure": 1031,
            "humidity": 32,
            "min_temp": 2.81,
            "max_temp": 2.81
        }, ...
    ]
}
```

 
 **Error Response:**

```json
{
    "success": false,
    "code": 404,
    "message": "Not Found"
}
```

# **Get Weather Information by City Name**

  Returns json data about given city weather information(s)

  -----

 **URL**

  `http://127.0.0.1:8000/api/weather/?city=Tashkent`

 **Method:**

  `GET`

  **Url Params**

  `Required: city`

 **Success Response:**

```json
{
    "success": true,
    "code": 200,
    "message": "OK",
    "data": [
        {
            "id": 1,
            "city": "Tashkent",
            "time": "2023-01-21 15:00:02",
            "weather_name": "Clouds",
            "temperature": 2.81,
            "pressure": 1031,
            "humidity": 32,
            "min_temp": 2.81,
            "max_temp": 2.81
        },
        {
            "id": 133,
            "city": "Tashkent",
            "time": "2023-01-21 17:00:02",
            "weather_name": "Clouds",
            "temperature": 0.88,
            "pressure": 1031,
            "humidity": 37,
            "min_temp": 0.88,
            "max_temp": 0.88
        }
    ]
}
```

 
 **Error Responses:**

```json
{
    "success": false,
    "code": 407,
    "message": "Current City Not Found"
}
```
or

```json
{
    "success": false,
    "code": 406,
    "message": "This City Weather Information Not Found"
}
```

---

## **If you have any questions about my APIs:**

Connect with me here:

[![Linkedin Badge](https://img.shields.io/badge/-Orifjon_Oripov-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/orifjon-orifov-a17125212/)](https://www.linkedin.com/in/orifjon-orifov-a17125212/) 
[![Telegram Badge](https://img.shields.io/badge/@orifjon_oripov-2CA5E0?style=flat-square&logo=telegram&logoColor=white&link=https://t.me/orifjon_oripov)](https://t.me/orifjon_oripov)



