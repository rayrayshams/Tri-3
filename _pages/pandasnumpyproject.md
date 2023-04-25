---
layout: page
title: Data Analysis Project
permalink: /DataAnalysisProject/
---

<html>
<table id="myTable">
  <thead>
    <tr>
      <th onclick="sortTable(0)">Name</th>
      <th onclick="sortTable(1)">Age</th>
      <th onclick="sortTable(2)">City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>35</td>
      <td>New York</td>
    </tr>
    <tr>
      <td>Mary</td>
      <td>25</td>
      <td>Los Angeles</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>40</td>
      <td>Chicago</td>
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