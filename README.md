# Geocoding
[![Visual Studio Code](https://custom-icon-badges.demolab.com/badge/Visual%20Studio%20Code-0078d7.svg?logo=vsc&logoColor=white)](#)
![ArcGIS](https://img.shields.io/badge/ArcGIS-Mapping%20&%20GIS-0079C1?logo=esri&logoColor=white)
![Komoot](https://img.shields.io/badge/Komoot-Outdoor%20Navigation-6AA84F?logo=komoot&logoColor=white)
[![Markdown](https://img.shields.io/badge/Markdown-%23000000.svg?logo=markdown&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This Python script reads addresses from a CSV file, processes them using geocoding services (ArcGIS and Komoot), and saves the results with latitude and longitude coordinates.

## Features
- Reads addresses from a CSV file
- Uses ArcGIS and Komoot geocoding services
- Implements retry logic for failed requests
- Saves output CSV files at defined intervals
- Handles missing data and errors gracefully

## Requirements
Ensure you have the following installed:
- Python 3.x

- Required Python libraries:
  sh
  pip install pandas requests geocoder

## Configuration
Modify the following parameters in the script to suit your needs:
- `input_file_path`: Path to the input CSV file containing addresses
- `output_dir`: Directory where the results will be saved
- `address_column_name`, `city_column_name`, `plz_column_name`: Define column names
- `start_index`: Start processing from a specific row (useful for resuming after a crash)
- `status_rate`: Print progress after processing every N addresses
- `write_data_rate`: Write intermediate results to a file after every N processed addresses
- `attempts_to_geocode`: Number of retries before giving up on an address
- `wait_time`: Initial delay before retrying failed requests

## Usage
1. Prepare your CSV file with columns for address, city, and optionally postal codes.
2. Run the script:
   sh
   python geo_calc.py
   
3. Results will be saved in the `output_test_coord` directory.

## Output
The script generates CSV files containing:
- Address
- Latitude
- Longitude
- Geocoding Provider

## Error Handling
- If an address cannot be geocoded, it is marked as "not geocoded".
- Errors are logged, and failed attempts are retried with a delay.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contributions
Feel free to open issues or submit pull requests for improvements.

<div align="right">

[Back To Top ⬆️](#Geocoding)
</div>

