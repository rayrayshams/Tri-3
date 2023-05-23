---
layout: page
title: Test Frontend
permalink: /TEST/
---

<html>
<head>
    <title>NBA Team Stats</title>
</head>
<body>
    <h1>NBA Team Stats</h1>
    <label for="team-select">Select a team:</label>
    <select id="team-select">
        <option value="">-- Select Team --</option>
        <option value="lakers">Los Angeles Lakers</option>
        <option value="warriors">Golden State Warriors</option>
        <option value="celtics">Boston Celtics</option>
        <!-- Add more options for other teams -->
    </select>
    <br><br>
    <iframe id="player-stats" width="100%" height="500px"></iframe>
    <script>
        var teamSelect = document.getElementById("team-select");
        var playerStats = document.getElementById("player-stats");
        teamSelect.addEventListener("change", function() {
            var team = this.value;
            if (team !== "") {
                var csvFile = team + ".csv"; // Assuming the CSV files are named after the teams (e.g., Lakers.csv)
                playerStats.setAttribute("src", csvFile);
            } else {
                playerStats.removeAttribute("src");
            }
        });
    </script>
</body>
</html>
