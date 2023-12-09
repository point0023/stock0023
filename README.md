<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stocks Webpage</title>
</head>
<body>

    <label for="stockDropdown">Select a stock:</label>
    <select id="stockDropdown" onchange="loadSelectedLink()">
        <option value="">Select a stock</option>
        <option value="https://chartink.com/stocks-new?&symbol=DBSTOCKBRO">DBSTOCKBRO</option>
        <option value="https://chartink.com/stocks-new?&symbol=INDBANK">INDBANK</option>
        <!-- Add more options for other stocks -->
    </select>

    <iframe id="selectedIframe" style="width: 100%; height: 600px; border: none;"></iframe>

    <script>
        function loadSelectedLink() {
            var dropdown = document.getElementById("stockDropdown");
            var selectedIframe = document.getElementById("selectedIframe");

            // Get the selected value from the dropdown
            var selectedValue = dropdown.value;

            // Set the source of the iframe to the selected link
            selectedIframe.src = selectedValue;
        }
    </script>

</body>
</html>
