---
layout: page
title: Pandas and Numpy Table Project
permalink: /pandas&numpyProject/
---

<html>
<table>
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
    <td>25</td>
    <td>New York</td>
    </tr>
    <tr>
    <td>Bob</td>
    <td>30</td>
    <td>Paris</td>
    </tr>
    <tr>
    <td>Alice</td>
    <td>20</td>
    <td>London</td>
    </tr>
</tbody>
</table>

<script>
    function sortTable(columnIndex) {
        let table = document.querySelector('table');
        let rows = Array.from(table.rows).slice(1); // ignore the header row
        let ascending = true;
  
        rows.sort((rowA, rowB) => {
            let cellA = rowA.cells[columnIndex].textContent;
            let cellB = rowB.cells[columnIndex].textContent;
    
            if (cellA < cellB) {
            return ascending ? -1 : 1;
            } else if (cellA > cellB) {
            return ascending ? 1 : -1;
            } else {
            return 0;
            }
        });
  
        // Remove existing rows from table and add sorted rows
        rows.forEach(row => table.tBodies[0].appendChild(row));
  
        // Toggle sort order for next click
        ascending = !ascending;
    }
</script>

</html>