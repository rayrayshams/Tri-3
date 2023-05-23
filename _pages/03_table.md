




<!DOCTYPE html>
<html>
<head>
  <title>CSV to HTML Table</title>
  <style>
    table {
      border-collapse: collapse;
      width: 100%;
    }
    th, td {
      border: 1px solid black;
      padding: 8px;
      text-align: left;
    }
    th {
      background-color: #f2f2f2;
    }
  </style>
</head>
<body>
  <h1>CSV to HTML Table</h1>

  <table id="csvTable">
    <!-- Table content will be dynamically generated here -->
  </table>

  <script>
    // Function to convert CSV to HTML table
    function csvToTable(csv) {
      var lines = csv.split("\n");
      var tableHTML = "<thead><tr>";
      var headers = lines[0].split(",");

      // Generate table headers
      for (var i = 0; i < headers.length; i++) {
        tableHTML += "<th>" + headers[i] + "</th>";
      }
      tableHTML += "</tr></thead><tbody>";

      // Generate table rows
      for (var j = 1; j < lines.length; j++) {
        var cells = lines[j].split(",");
        tableHTML += "<tr>";
        for (var k = 0; k < cells.length; k++) {
          tableHTML += "<td>" + cells[k] + "</td>";
        }
        tableHTML += "</tr>";
      }
      tableHTML += "</tbody>";

      return tableHTML;
    }

    // Read the CSV file and generate the HTML table
    function readCSV(file) {
      var reader = new FileReader();
      reader.onload = function (e) {
        var csv = e.target.result;
        var htmlTable = csvToTable(csv);
        document.getElementById("csvTable").innerHTML = htmlTable;
      };
      reader.readAsText(file);
    }

    // Handle file input change event
    function handleFileSelect(event) {
      var file = event.target.files[0];
      readCSV(file);
    }

    // Attach event listener to the file input element
    document.getElementById("csvFile").addEventListener("change", handleFileSelect, false);
  </script>

  <input type="file" id="csvFile" accept=".csv">

  <script>
    // Automatically load "wizards.csv" file on page load
    window.onload = function() {
      var file = new File([""], "T3Project/_notebooks/files/wizards.csv");
      readCSV(file);
    };
  </script>

</body>
</html>
