---
layout: page
title: Data Analysis Project
permalink: /DataAnalysisProject/
---

### Click the table headers to sort the entries in descending order. Click the table headers again to reverse the order.

<html>
<table id="myTable">
  <thead>
    <tr>
      <th onclick="sortTable(0)">Team Name</th>
      <th onclick="sortTable(1)">Year Founded</th>
      <th onclick="sortTable(2)">Championships Won</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Atlanta Hawks</td>
      <td>1949</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Boston Celtics</td>
      <td>1946</td>
      <td>17</td>
    </tr>
    <tr>
      <td>Brooklyn Nets</td>
      <td>1976</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Charlotte Hornets</td>
      <td>1988</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Chicago Bulls</td>
      <td>1966</td>
      <td>06</td>
    </tr>
    <tr>
      <td>Cleveland Cavaliers</td>
      <td>1970</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Dallas Mavericks</td>
      <td>1980</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Denver Nuggets</td>
      <td>1976</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Detroit Pistons</td>
      <td>1948</td>
      <td>03</td>
    </tr>
    <tr>
      <td>Golden State Warriors</td>
      <td>1946</td>
      <td>07</td>
    </tr>
    <tr>
      <td>Houton Rockets</td>
      <td>1967</td>
      <td>02</td>
    </tr>
    <tr>
      <td>Indiana Pacers</td>
      <td>1976</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Los Angeles Clippers</td
      ><td>1970</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Los Angeles Lakers</td>
      <td>1948</td>
      <td>17</td>
    </tr>
    <tr>
      <td>Memphis Grizzlies</td>
      <td>1995</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Miami Heat</td>
      <td>1988</td>
      <td>03</td>
    </tr>
    <tr>
      <td>Milwaukee Bucks</td>
      <td>1968</td>
      <td>02</td>
    </tr>
    <tr>
      <td>Minnesota Timberwolves</td>
      <td>1989</td>
      <td>00</td>
    </tr>
    <tr>
      <td>New Orleans Pelicans</td>
      <td>2002</td>
      <td>00</td>
    </tr>
    <tr>
      <td>New York Knicks</td>
      <td>1946</td>
      <td>02</td>
    </tr>
    <tr>
      <td>Oklahoma City Thunder</td>
      <td>1967</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Orlando Magic</td>
      <td>1989</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Philadelphia 76ers</td>
      <td>1949</td>
      <td>03</td>
    </tr>
    <tr>
      <td>Phoenix Suns</td>
      <td>1968</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Portland Trail Blazers</td>
      <td>1970</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Sacramento Kings</td>
      <td>1948</td>
      <td>00</td>
    </tr>
    <tr>
      <td>San Antonio Spurs</td>
      <td>1976</td>
      <td>05</td>
    </tr>
    <tr>
      <td>Toronto Raptors</td>
      <td>1995</td>
      <td>01</td>
    </tr>
    <tr>
      <td>Utah Jazz</td>
      <td>1974</td>
      <td>00</td>
    </tr>
    <tr>
      <td>Washington Wizards</td>
      <td>1961</td>
      <td>01</td>
    </tr>
  </tbody>
</table>

<script>
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
</html>