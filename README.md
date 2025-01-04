# Weather Data API App

This Python application provides a web-based interface and API to access historical weather data, including temperature records for specific stations and dates.

## Prerequisites

* Python 3.x

* Flask

* Pandas

## Usage

1. Clone the repository and ensure the following files are present:
   
* `main.py` (the Flask application)
* `data_small/` (directory containing weather data files)
* `templates/home.html` (HTML template for the home page)
  
2. Install all dependencies:
   
   ```bash
   pip install -r requirements.txt
   ```
(If requirements.txt is not provided, manually install Flask and Pandas:)

``` bash
pip install flask pandas
```

3. Run the Flask application:
   
```bash
python main.py
```

4. Open your browser and navigate to:
   
```bash
http://127.0.0.1:5002/
```

## Description

 **Application Files**

* `main.py`: The main Flask application containing routes to serve the weather data.

* `data_small/`: Directory containing station metadata (stations.txt) and temperature records (TG_STAIDxxxxxx.txt).

* `templates/home.html`: HTML template for the home page displaying station data.

 **API Endpoints**

1. **Home Page**

* URL: /
  
* Displays a table of station data.

2. **Get temperature for a Specific Station and Date**
   
* URL: /api/v1/<station>/<date>

* Example: /api/v1/10/1988-10-25

* Returns the temperature for a specific station on a given date.

3. **Get all Data for a Specific Station**
   
* URL: /api/v1/<station>

* Example: /api/v1/10

* Returns all temperature data for the specified station.

5. **Get yearly Data for a Specific Station**
   
* URL: /api/v1/yearly/<station>/<year>
 
* Example: /api/v1/yearly/10/1988

* Returns temperature data for a specific station and year.

## How It Works

* Station data is stored in `data_small/stations.txt`.

* Temperature records are in files like `TG_STAIDxxxxxx.txt`.
  
* Flask serves the data through the API endpoints.

## Configuration

* Ensure all data files are placed in the `data_small/ directory`.
  
* Adjust the port or debug settings in `main.py` if needed:
```bash
app.run(debug=True, port=5002)
```

## Notes

* Temperature values are stored as tenths of a degree Celsius and converted to degrees in the API response.
  
* The app provides a simple interface to access and query weather data.
  
* Use the API endpoints to integrate weather data into other applications.

## Author 

Priya Patel 

Github: priyap243
