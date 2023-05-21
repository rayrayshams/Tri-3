---
layout: page
title: Project
permalink: /Project/
---
<html>
<head>
    <style>
        /* CSS for dropdown menus */
        .dropdown1 {
            position: relative;
            display: inline-block;
            margin-right: 300px;
            margin-bottom: 150px;
            border: 1px solid black;
            background-color: #C9082A;
            width: 300px;
            box-shadow: 0px 10px 20px rgba(0,0,0,0.5);
            border-radius: 15px;
            padding: 15px;
            text-align: center;
            font-size: 22px;
            cursor: pointer;
            background: linear-gradient(to top right, #C1082A, #D3082A);
        }
        .dropdown {
            position: relative;
            display: inline-block;
            margin-right: 300px;
            margin-bottom: 150px;
            border: 1px solid black;
            background-color: #C9082A;
            width: 300px;
            box-shadow: 0px 10px 20px rgba(0,0,0,0.5);
            border-radius: 15px;
            padding: 15px;
            text-align: center;
            font-size: 22px;
            cursor: pointer;
            background: linear-gradient(to top right, #C1082A, #D3082A);
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
            width: 200px;
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
</head>
<body>
    <div class="dropdown">
        <span>Pick a Team</span>
        <div class="dropdown-content">
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
            <div class="dropdown-item" id="team11">Houton Rockets</div>
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
</body>
</html>