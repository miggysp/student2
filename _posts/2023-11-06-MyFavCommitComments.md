<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather Application</title>
    <style>
        /* Styling for the page */
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            text-align: center;
            padding: 20px;
            border: 2px solid #ddd;
            border-radius: 5px;
            width: 300px;
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            box-sizing: border-box;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .button-container {
            display: flex;
            justify-content: space-between;
        }
        .button-container button {
            background-color: #4CAF50;
            color: white;
            padding: 5px 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            flex: 1;
        }
        button:hover {
            background-color: #45a049;
        }
        #result {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .button-spacing {
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Switch for Metric Units -->
        <label class="switch">
            <input type="checkbox" id="tempSwitch" onclick="getMetric()">
            <span class="slider round"></span>
        </label>
        <span id="tempLabel">Metric Units</span>
        <h2>Weather Application</h2>
        <img src="https://backend.stu.nighthawkcodingsociety.com/static/assets/sunny_weather.png" id="weatherIcon" height="200" width="200">
        //Checkbox that runs the function "is Metric" On click
        <input type="text" id="location" placeholder="Enter city name" autofocus onkeyup="handleKeyPress(event)">
        <div class="button-container">
            <button class="button-spacing" onclick="getWindSpeed()">Wind Speed</button>
            <button class="button-spacing" onclick="getTemperature()">Temperature</button>
            <button class="button-spacing" onclick="getPrecipitation()">Precipitation</button>
        </div>
        <div id="result"></div>
    </div>
    <script>
        // Initialize a flag for metric units
        let isMetric = false; // Define it as false to begin with b/c non-metric should be a default mode for most people who will use our code 

        // Function to handle Enter key press
        function handleKeyPress(event) {
            if (event.key === 'Enter') {
                // Handle Enter key press here (currently no action specified)
            }
        }

        // Function to fetch Wind Speed data
        function getWindSpeed() {
            fetchWeatherData('wind_mph');
        }

        // Function to fetch Temperature data
        function getTemperature() {
            fetchWeatherData('feelslike_f');
        }

        // Function to fetch Precipitation data
        function getPrecipitation() {
            fetchWeatherData('precip_in');
        }

        // Capitalize the first letter of a string
        function capitalizeFirstLetter(string) {
            return string.charAt(0).toUpperCase() + string.slice(1);
        }

        // Toggle between Metric and Imperial units
        function getMetric() {
            isMetric = !isMetric;
            // toggle isMetric true or false based on the checkbox being clicked 
        }

        // Function to fetch weather data from an API
        function fetchWeatherData(dataType) {
            const locationInput = document.getElementById('location');
            const resultDiv = document.getElementById('result');
            const location = capitalizeFirstLetter(locationInput.value.trim());

            if (location === '') {
                resultDiv.innerText = 'Please enter a location';
                return;
            }

            resultDiv.innerText = 'Loading...';

            // Fetch weather data from an API
            fetch('https://backend.stu.nighthawkcodingsociety.com/api/weather/' + location)
                .then(response => response.json())
                .then(data => {
                    // Fetch an image URL based on the location
                    let imageFetchUrl = 'https://backend.stu.nighthawkcodingsociety.com/api/cityimage/' + location;
                    fetch(imageFetchUrl)
                        .then(response => response.json())
                        .then(imageData => {
                            // Get the URL of the weather icon
                            let imageUrl = imageData.image_url;
                            console.log("IMAGE_URL====" + imageUrl);
                            var image = document.getElementById('weatherIcon');
                            image.src = data["current"]["weatherIcon_url"];

                            if (dataType === 'wind_mph' && isMetric === true) { // 3 trues, and 3 falses
                                resultDiv.innerHTML = `<h2>Current Wind Speed in ${location} is ${parseFloat(data["current"]["wind_mph"] * 1.61).toFixed(2)} KPH </h2>`;
                            } else if (dataType === 'feelslike_f' && isMetric === true) {
                                resultDiv.innerHTML = `<h2>Current Temperature in ${location} is ${parseFloat((data["current"]["feelslike_f"] - 32) * (0.55)).toFixed(2)} °C</h2>`;
                            } else if (dataType === 'precip_in' && isMetric === true) {
                                resultDiv.innerHTML = `<h2>Current Precipitation in ${location} is ${parseFloat(data["current"]["precip_in"] * 2.54).toFixed(2)} cm</h2>`;
                            } else if (dataType === 'wind_mph' && isMetric === false) {
                                resultDiv.innerHTML = `<h2>Current Wind Speed in ${location} is ${data["current"]["wind_mph"]} MPH </h2>`;
                            } else if (dataType === 'feelslike_f' && isMetric === false) {
                                resultDiv.innerHTML = `<h2>Current Temperature in ${location} is ${data["current"]["feelslike_f"]} °F</h2>`;
                            } else if (dataType === 'precip_in' && isMetric === false) {
                                resultDiv.innerHTML = `<h2>Current Precipitation in ${location} is ${data["current"]["precip_in"]} inches</h2>`;
                            }

                            // Create an image element and set its source
                            let imgElement = document.createElement('img');
                            imgElement.src = imageUrl;
                            resultDiv.appendChild(imgElement);
                        })
                        .catch(error => {
                            console.error('Error fetching image:', error);
                            resultDiv.innerText += 'An error occurred fetching the image. Please try again later.';
                        });
                })
                .catch(error => {
                    console.error('Error fetching data:', error);
                    resultDiv.innerText = 'An error occurred. Please try again later.';
                });
        }
    </script>
</body>
</html>
