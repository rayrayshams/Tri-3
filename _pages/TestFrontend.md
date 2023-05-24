---
layout: page
title: Test Frontend
permalink: /TEST/
---

<!-- CSS -->
<style type="text/css">
    table th, table td{
    padding: 5px;
}
</style>

<div>
    <div>
         <input type="file" name="file" id="file" accept=".csv" > <br><br>
         <input type="button" id="btnsubmit" value="Submit" onclick="readCSVFile();" >
    </div>
    <br><br>
    <!-- List CSV file data -->
    <table id="tblcsvdata" border="1" style="border-collapse: collapse;">
         <thead>
              <tr>
                  <th onclick="sortTable(0)">Name</th>
                  <th onclick="sortTable(1)">Games Played</th>
                  <th onclick="sortTable(2)">Points</th>
                  <th onclick="sortTable(3)">Assists</th>
                  <th onclick="sortTable(4)">Rebounds</th>
                  <th onclick="sortTable(5)">Steals</th>
                  <th onclick="sortTable(6)">Blocks</th>
                  <th onclick="sortTable(7)">Field Goal %</th>
                  <th onclick="sortTable(8)">3 Point %</th>
              </tr>
         </thead>
         <tbody>
         </tbody>
    </table>
</div>

<script>
    function readCSVFile(){
     var files = document.querySelector('#file').files;

     if(files.length > 0 ){

          // Selected file
          var file = files[0];

          // FileReader Object
          var reader = new FileReader();

          // Read file as string 
          reader.readAsText(file);

          // Load event
          reader.onload = function(event) {

               // Read file data
               var csvdata = event.target.result;

               // Split by line break to gets rows Array
               var rowData = csvdata.split('\n');

               // <table > <tbody>
               var tbodyEl = document.getElementById('tblcsvdata').getElementsByTagName('tbody')[0];
               tbodyEl.innerHTML = "";

               // Loop on the row Array (change row=0 if you also want to read 1st row)
               for (var row = 1; row < rowData.length; row++) {

                     // Insert a row at the end of table
                     var newRow = tbodyEl.insertRow();

                     // Split by comma (,) to get column Array
                     rowColData = rowData[row].split(',');

                     // Loop on the row column Array
                     for (var col = 0; col < rowColData.length; col++) {

                          // Insert a cell at the end of the row
                          var newCell = newRow.insertCell();
                          newCell.innerHTML = rowColData[col];

                     }

               }
          };

     }else{
          alert("Please select a file.");
     }

}

     function sortTable(columnIndex) {
          const table = document.getElementById("myTable");
          const tbody = table.getElementsByTagName("tbody")[0];
          const rows = tbody.getElementsByTagName("tr");
          const sortDirection = getSortDirection(columnIndex);

          const sortedRows = Array.from(rows)
          .sort((rowA, rowB) => {
               const cellA = rowA.getElementsByTagName("td")[columnIndex];
               const cellB = rowB.getElementsByTagName("td")[columnIndex];
               return compareCells(cellA, cellB, sortDirection);
          });

          for (const row of sortedRows) {
               tbody.appendChild(row);
          }
     }

     function getSortDirection(columnIndex) {
          const table = document.getElementById("myTable");
          const headerRow = table.getElementsByTagName("thead")[0].getElementsByTagName("tr")[0];
          const headerCell = headerRow.getElementsByTagName("th")[columnIndex];

          if (headerCell.getAttribute("data-sort-direction") === "asc") {
               headerCell.setAttribute("data-sort-direction", "desc");
          return "desc";
          } else {
               headerCell.setAttribute("data-sort-direction", "asc");
          return "asc";
          }
     }

     function compareCells(cellA, cellB, sortDirection) {
     const valueA = cellA.textContent.trim();
     const valueB = cellB.textContent.trim();

     if (sortDirection === "asc") {
          if (valueA < valueB) {
               return -1;
          } else if (valueA > valueB) {
               return 1;
          } else {
               return 0;
          }
          } else {
          if (valueA < valueB) {
               return 1;
          } else if (valueA > valueB) {
               return -1;
          } else {
               return 0;
          }
          }
     }
</script>