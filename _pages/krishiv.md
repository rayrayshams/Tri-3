---
layout: page
title: Fake
permalink: /FakeProject/
---
<html>
<head>
   <style>
       /* CSS for dropdown menus */
       .dropdown1 {
           position: relative;
           display: inline-block;
           margin-right: 30px;
           border: 1px solid black;
           background-color: #C9082A;
           width: 250px;
           box-shadow: 0px 10px 20px rgba(0,0,0,0.5);
           border-radius: 15px;
           padding: 15px;
           text-align: center;
           font-size: 22px;
           cursor: pointer;
           background: linear-gradient(to top right, #DD0303, #FB7373);
       }
       .dropdown {
           position: relative;
           display: inline-block;
           margin-right: 30px;
           border: 1px solid black;
           background-color: #C9082A;
           width: 250px;
           box-shadow: 0px 10px 20px rgba(0,0,0,0.5);
           border-radius: 15px;
           padding: 15px;
           text-align: center;
           font-size: 22px;
           cursor: pointer;
           background: linear-gradient(to top right, #DD0303, #FB7373);
       }
       .dropdown-content {
           display: none;
           position: absolute;
           background-color: #f9f9f9;
           width: 600px;
           z-index: 1;
           box-shadow: 0px 10px 20px rgba(0,0,0,0.8);
           border-radius: 8px;
           padding: 12px;
           font-size: 15px;
           column-count: 3;
           column-gap: 0.5px;
           text-align: center;
       }
       .dropdown:hover .dropdown-content {
           display: block;
       }
       .dropdown-item {
           padding: 10px;
           color: #333;
           cursor: pointer;
           transition: background-color 0.3s ease;
       }
       .dropdown-item:hover {
           background-color: #e5e5e5;
       }
       .dropdown-item:first-child {
           margin-top: 0;
       }
       .dropdown-item:last-child {
           margin-bottom: 0;
       }
       .dropdown-content1 {
           display: none;
           font-size: 15px;
           position: absolute;
           background-color: #f9f9f9;
           width: 230px;
           z-index: 1;
           box-shadow: 0px 10px 20px rgba(0,0,0,0.8);
           border-radius: 8px;
           padding: 12px;
           column-count: 2;
           column-gap: 0.5px;
           text-align: center;
       }
       .dropdown1:hover .dropdown-content1 {
           display: block;
       }
       .dropdown-item1 {
           padding: 10px;
           color: #333;
           cursor: pointer;
           transition: background-color 0.3s ease;
       }
       .dropdown-item1:hover {
           background-color: #e5e5e5;
       }
       .dropdown-item1:first-child {
           margin-top: 0;
       }
       .dropdown-item1:last-child {
           margin-bottom: 0;
       }
   </style>
   <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
   <div class="dropdown">
       <span>Pick a Team</span>
       <div class="dropdown-content">
           <div class="dropdown-item" id="team0">All Players</div>
           <div class="dropdown-item" id="team1">Atlanta Hawks</div>
           <div class="dropdown-item" id="team2">Boston Celtics</div>
           <div class="dropdown-item" id="team3">Brooklyn Nets</div>
           <div class="dropdown-item" id="team4">Charlotte Hornets</div>
           <div class="dropdown-item" id="team5">Chicago Bulls</div>
           <div class="dropdown-item" id="team6">Cleveland Cavaliers</div>
           <div class="dropdown-item" id="team7">Dallas Mavericks</div>
           <div class="dropdown-item" id="team8">Denver Nuggets</div>
           <div class="dropdown-item" id="team9">Detroit Pistons</div>
           <div class="dropdown-item" id="team10">Golden State Warriors</div>
           <div class="dropdown-item" id="team11">Houston Rockets</div>
           <div class="dropdown-item" id="team12">Indiana Pacers</div>
           <div class="dropdown-item" id="team13">Los Angeles Clippers</div>
           <div class="dropdown-item" id="team14">Los Angeles Lakers</div>
           <div class="dropdown-item" id="team15">Memphis Grizzlies</div>
           <div class="dropdown-item" id="team16">Miami Heat</div>
           <div class="dropdown-item" id="team17">Milwaukee Bucks</div>
           <div class="dropdown-item" id="team18">Minnesota Timberwolves</div>
           <div class="dropdown-item" id="team19">New Orleans Pelicans</div>
           <div class="dropdown-item" id="team20">New York Knicks</div>
           <div class="dropdown-item" id="team21">Oklahoma City Thunder</div>
           <div class="dropdown-item" id="team22">Orlando Magic</div>
           <div class="dropdown-item" id="team23">Philadelphia 76ers</div>
           <div class="dropdown-item" id="team24">Phoenix Suns</div>
           <div class="dropdown-item" id="team25">Portland Trail Blazers</div>
           <div class="dropdown-item" id="team26">Sacramento Kings</div>
           <div class="dropdown-item" id="team27">San Antonio Spurs</div>
           <div class="dropdown-item" id="team28">Toronto Raptors</div>
           <div class="dropdown-item" id="team29">Utah Jazz</div>
           <div class="dropdown-item" id="team30">Washington Wizards</div>
       </div>
   </div>
   <div class="dropdown1">
       <span>Pick a Stat - Bar Graph</span>
       <div class="dropdown-content1">
           <div class="dropdown-item1" id="bar1">Points</div>
           <div class="dropdown-item1" id="bar2">Assists</div>
           <div class="dropdown-item1" id="bar3">Rebounds</div>
           <div class="dropdown-item1" id="bar4">Steals</div>
           <div class="dropdown-item1" id="bar5">Blocks</div>
           <div class="dropdown-item1" id="bar6">Field Goal %</div>
           <div class="dropdown-item1" id="bar7">3 Point %</div>
       </div>
   </div>
   <div class="dropdown1">
       <span>Pick a Stat - Pie Graph</span>
       <div class="dropdown-content1">
           <div class="dropdown-item1" id="pie1">Points</div>
           <div class="dropdown-item1" id="pie2">Assists</div>
           <div class="dropdown-item1" id="pie3">Rebounds</div>
           <div class="dropdown-item1" id="pie4">Steals</div>
           <div class="dropdown-item1" id="pie5">Blocks</div>
           <div class="dropdown-item1" id="pie6">Field Goal %</div>
           <div class="dropdown-item1" id="pie7">3 Point %</div>
       </div>
   </div>
   <br>
   <br>
   <br>
   <br>
   <br>
   <div id="table"></div>
   <br>
   <div id="barGraph"></div>
   <br>
   <div id="pieGraph"></div>

<script>

   const tableContainer = document.getElementById("table");
   const barGraphContainer = document.getElementById("barGraph");
   const pieGraphContainer = document.getElementById("pieGraph");
      
   fetch('https://petitepandas.duckdns.org/api/graphs/')
     .then(response => response.json())
     .then(data => {
           var tableData = data;
           var barGraphData = null;
           var pieGraphData = null;
           // Add event listeners for each team
           document.getElementById('team0').addEventListener('click', () => displayAll(tableData));
           document.getElementById('team1').addEventListener('click', () => displayTable('hawks'));
           document.getElementById('team2').addEventListener('click', () => displayTable('celtics'));
           document.getElementById('team3').addEventListener('click', () => displayTable('nets'));
           document.getElementById('team4').addEventListener('click', () => displayTable('hornets'));
           document.getElementById('team5').addEventListener('click', () => displayTable('bulls'));
           document.getElementById('team6').addEventListener('click', () => displayTable('cavaliers'));
           document.getElementById('team7').addEventListener('click', () => displayTable('mavericks'));
           document.getElementById('team8').addEventListener('click', () => displayTable('nuggets'));
           document.getElementById('team9').addEventListener('click', () => displayTable('pistons'));
           document.getElementById('team10').addEventListener('click', () => displayTable('warriors'));
           document.getElementById('team11').addEventListener('click', () => displayTable('rockets'));
           document.getElementById('team12').addEventListener('click', () => displayTable('pacers'));
           document.getElementById('team13').addEventListener('click', () => displayTable('clippers'));
           document.getElementById('team14').addEventListener('click', () => displayTable('lakers'));
           document.getElementById('team15').addEventListener('click', () => displayTable('grizzlies'));
           document.getElementById('team16').addEventListener('click', () => displayTable('heat'));
           document.getElementById('team17').addEventListener('click', () => displayTable('bucks'));
           document.getElementById('team18').addEventListener('click', () => displayTable('timberwolves'));
           document.getElementById('team19').addEventListener('click', () => displayTable('pelicans'));
           document.getElementById('team20').addEventListener('click', () => displayTable('knicks'));
           document.getElementById('team21').addEventListener('click', () => displayTable('thunder'));
           document.getElementById('team22').addEventListener('click', () => displayTable('magic'));
           document.getElementById('team23').addEventListener('click', () => displayTable('76ers'));
           document.getElementById('team24').addEventListener('click', () => displayTable('suns'));
           document.getElementById('team25').addEventListener('click', () => displayTable('blazers'));
           document.getElementById('team26').addEventListener('click', () => displayTable('kings'));
           document.getElementById('team27').addEventListener('click', () => displayTable('spurs'));
           document.getElementById('team28').addEventListener('click', () => displayTable('raptors'));
           document.getElementById('team29').addEventListener('click', () => displayTable('jazz'));
           document.getElementById('team30').addEventListener('click', () => displayTable('wizards'));

     
   function selectTeam(teamName) {

       barGraphData = tableData[teamName];
       pieGraphData = tableData[teamName];
       barGraphContainer.innerHTML = ''
       pieGraphContainer.innerHTML = ''
       //displayBarGraph("Points")
       //displayPieGraph("Points")
   }

   function displayAll(tableData){
       //alert("display all");
       tableData.forEach((v) => {
           //alert("team:",v.teamName);
           displayTable(v.teamName);

       });

   }


   function displayTable(teamName) {
       var team = teamName;
       const data = tableData[teamName]; //display_table(teamName);
       const tableElement = document.getElementById('table');
       const table = document.createElement('table');

       const teamNameRow = document.createElement('tr');
       teamNameRow.textContent = teamName;
       table.appendChild(teamNameRow);

       const headerRow = document.createElement('tr');
       // Create the table header row
       for (const column of Object.keys(data)) {
           const headerCell = document.createElement('th');
           headerCell.textContent = column;
           headerRow.appendChild(headerCell);
       }
       table.appendChild(headerRow);

       // Iterate over the keys of the Player object and retrieve the corresponding data
       //alert(Object.values(data[0]));
       const playerKeys = Object.keys(data['Player']);
       for (const key of playerKeys) {
           const bodyRow = document.createElement('tr');
           for (const column of Object.keys(data)) {
           const bodyCell = document.createElement('td');
           bodyCell.textContent = data[column][key];
           bodyRow.appendChild(bodyCell);
           }
           table.appendChild(bodyRow);
       };


       // Clear the table element and append the new table
       tableElement.innerHTML = '';
       tableElement.appendChild(table);
       selectTeam(teamName);
       //test code
       //alert("call graph display_table method");
       display_table(teamName);
       //alert("after graph display_table method ");
   };
  
   document.getElementById('bar1').addEventListener('click', () => displayBarGraph('Points'));
   document.getElementById('bar2').addEventListener('click', () => displayBarGraph('Assists'));
   document.getElementById('bar3').addEventListener('click', () => displayBarGraph('Rebounds'));
   document.getElementById('bar4').addEventListener('click', () => displayBarGraph('Steals'));
   document.getElementById('bar5').addEventListener('click', () => displayBarGraph('Blocks'));
   document.getElementById('bar6').addEventListener('click', () => displayBarGraph('FG%'));
   document.getElementById('bar7').addEventListener('click', () => displayBarGraph('3PT%'));
          
   document.getElementById('pie1').addEventListener('click', () => displayPieGraph('Points'));
   document.getElementById('pie2').addEventListener('click', () => displayPieGraph('Assists'));
   document.getElementById('pie3').addEventListener('click', () => displayPieGraph('Rebounds'));
   document.getElementById('pie4').addEventListener('click', () => displayPieGraph('Steals'));
   document.getElementById('pie5').addEventListener('click', () => displayPieGraph('Blocks'));
   document.getElementById('pie6').addEventListener('click', () => displayPieGraph('FG%'));
   document.getElementById('pie7').addEventListener('click', () => displayPieGraph('3PT%')); 

   function displayBarGraph(aspect) {
       const data = barGraphData;
       let trace = {
           x: Object.values(data.Player),
           y: Object.values(data[aspect]),
           type: 'bar'
       };

       let layout = {
           title: 'Player ' + aspect,
           xaxis: { title: 'Player' },
           yaxis: { title: aspect }
       };

       let graphData = [trace];

       Plotly.newPlot('barGraph', graphData, layout);
       };

   function displayPieGraph(aspect) {
       const data = pieGraphData;
       let trace = {
           labels: Object.values(data.Player),
           values: Object.values(data[aspect]),
           type: 'pie'
       };

       let layout = {
           title: aspect + ' Distribution by Players'
       };

       let graphData = [trace];

       Plotly.newPlot('pieGraph', graphData, layout);
       };
   })
   .catch(error => {
       console.log('Error message', error);
   });
</script>
<script>
headerCell.addEventListener('click', () => sortTable(column));

function sortTable(column) {
 const table = document.querySelector('table');
 const rows = Array.from(table.querySelectorAll('tr'));
  // Remove the current active class from the header cells
 const activeHeader = table.querySelector('.active');
 if (activeHeader) {
   activeHeader.classList.remove('active');
 }
  // Determine the sorting order (ascending or descending)
 const isAscending = !table.classList.contains('desc');
 table.classList.toggle('desc', isAscending);
  // Get the index of the column to be sorted
 const columnIndex = Array.from(table.querySelectorAll('th')).indexOf(column);
  // Sort the rows based on the column values
 rows.sort((a, b) => {
   const aValue = a.cells[columnIndex].textContent;
   const bValue = b.cells[columnIndex].textContent;
  
   if (isAscending) {
     return aValue.localeCompare(bValue);
   } else {
     return bValue.localeCompare(aValue);
   }
 });
  // Re-append the sorted rows to the table
 rows.forEach(row => table.appendChild(row));
  // Add the active class to the clicked header cell
 column.classList.add('active');
}

</script>


</body>
</html>

