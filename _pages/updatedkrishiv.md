---
layout: page
title: Updated Backend Test
---


<html>
<head>
  <title>Graphs</title>
  <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
  <div id="table"></div>
  <br>
  <div id="barGraph"></div>
  <br>
  <div id="pieGraph"></div>

  <script>
    // Fetch data from the API endpoint
    fetch('https://petitepandas.duckdns.org/api/graphs')
      .then(response => response.json())
      .then(data => {
        // Display the table
        displayTable(data);

        // Display the bar graph
        displayBarGraph(data);

        // Display the pie graph
        displayPieGraph(data);
      })
      .catch(error => console.log(error));

    function displayTable(data) {
      // Get the table element
      const tableElement = document.getElementById('table');

      // Create the table
      const table = document.createElement('table');

      // Create the table header row
      const headerRow = document.createElement('tr');
      for (const column of Object.keys(data)) {
        const headerCell = document.createElement('th');
        headerCell.textContent = column;
        headerCell.addEventListener('click', function() {
          sortTable(Array.from(headerRow.children).indexOf(headerCell));
        });
        headerRow.appendChild(headerCell);
      }
      table.appendChild(headerRow);

      // Iterate over the keys of the Player object and retrieve the corresponding data
      const playerKeys = Object.keys(data.Player);
      for (const key of playerKeys) {
        const bodyRow = document.createElement('tr');
        for (const column of Object.keys(data)) {
          const bodyCell = document.createElement('td');
          bodyCell.textContent = data[column][key];
          bodyRow.appendChild(bodyCell);
        }
        table.appendChild(bodyRow);
      }

      // Clear the table element and append the new table
      tableElement.innerHTML = '';
      tableElement.appendChild(table);
    }

    function displayBarGraph(data) {
      let trace = {
        x: Object.values(data.Player),
        y: Object.values(data.Points),
        type: 'bar'
      };

      let layout = {
        title: 'Player Points',
        xaxis: { title: 'Player' },
        yaxis: { title: 'Points' }
      };

      let graphData = [trace];

      Plotly.newPlot('barGraph', graphData, layout);
    };

    function displayPieGraph(data) {
      let trace = {
        labels: Object.values(data.Player),
        values: Object.values(data.Points),
        type: 'pie'
      };

      let layout = {
        title: 'Points Distribution by Players'
      };

      let graphData = [trace];

      Plotly.newPlot('pieGraph', graphData, layout);
    };

    function sortTable(columnIndex) {
      var table, rows, switching, i, x, y, shouldSwitch;
      table = document.querySelector('#table table');
      switching = true;

      while (switching) {
        switching = false;
        rows = table.rows;

        for (i = 1; i < (rows.length - 1); i++) {
          shouldSwitch = false;
          x = rows[i].getElementsByTagName("td")[columnIndex];
          y = rows[i + 1].getElementsByTagName("td")[columnIndex];

          if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
            shouldSwitch = true;
            break;
          }
        }
      }
    }