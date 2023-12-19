<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Machine Learning Web App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 50px;
    }
    #input-container {
      margin-bottom: 20px;
    }
    #result {
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div id="input-container">
    <label for="input">Enter a number:</label>
    <input type="number" id="input" />
    <button onclick="predict()">Predict</button>
  </div>

  <div>
    <p>Predicted Value:</p>
    <p id="result"></p>
  </div>

  <script>
    // Simple linear regression model
    function predict() {
      const inputValue = parseFloat(document.getElementById('input').value);
      // Replace these coefficients with your trained model's coefficients
      const intercept = 2.5;
      const slope = 1.7;
      const predictedValue = intercept + slope * inputValue;
      document.getElementById('result').innerText = predictedValue.toFixed(2);
    }
  </script>

</body>
</html>
