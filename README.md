<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        #container {
            margin: 50px auto;
            padding: 20px;
            width: 300px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #f4f4f4;
        }
        h1 {
            color: #333;
        }
        #result {
            font-size: 20px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1>Temperature Converter</h1>
        <label for="celsius">Enter temperature in Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter Celsius" oninput="convertTemperature()">
        <p id="result"></p>
    </div>

    <script>
        function convertTemperature() {
            const celsiusInput = document.getElementById("celsius").value;
            const fahrenheit = (celsiusInput * 9/5) + 32;
            const resultElement = document.getElementById("result");
            resultElement.textContent = `${celsiusInput}°C is equal to ${fahrenheit.toFixed(2)}°F`;
        }
    </script>
</body>
</html>
