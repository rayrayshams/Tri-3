---
layout: page
title: PLEASE WORK!
permalink: /okay/
---


<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.jsdelivr.net/npm/danfojs@0.1.1/dist/index.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@3.7.0/dist/chart.min.js"></script>
    <title>Document</title>
</head>
<body>
    <div id="plot_div"></div>
    <br>
    <div id="bar_plot"></div>
    <br>
    <div id="pie_plot" style="width: 400px; height: 300px;"></div>
    <script>
        dfd.read_csv("https://raw.githubusercontent.com/paravsalaniwal/T3Project/master/_notebooks/files/warriors.csv")
            .then(df => {
                var layout = {
                    title: 'WARRIORS CHART',
                    xaxis: {title: 'Player'},
                    yaxis: {title: 'Count'}
                };
                var barLayout = {
                    title: 'WARRIORS BAR CHART',
                    xaxis: {title: 'Player'},
                    yaxis: {title: 'Count'}
                };
                var pieData = {
                    labels: df.index,
                    datasets: [{
                        label: 'WARRIORS PIE CHART',
                        data: df.column("Points"),
                        backgroundColor: [
                            'rgba(255, 99, 132, 0.5)',
                            'rgba(54, 162, 235, 0.5)',
                            'rgba(255, 206, 86, 0.5)',
                            'rgba(75, 192, 192, 0.5)',
                            'rgba(153, 102, 255, 0.5)',
                        ],
                        borderColor: [
                            'rgba(255, 99, 132, 1)',
                            'rgba(54, 162, 235, 1)',
                            'rgba(255, 206, 86, 1)',
                            'rgba(75, 192, 192, 1)',
                            'rgba(153, 102, 255, 1)',
                        ],
                        borderWidth: 1
                    }]
                };
                df.plot("plot_div").line({ columns: ["Points"], layout: layout });
                df.plot("bar_plot").bar({ columns: ["Points"], layout: barLayout });
                new Chart(document.getElementById('pie_plot'), {
                    type: 'pie',
                    data: pieData,
                    options: {
                        responsive: true,
                        plugins: {
                            legend: {
                                position: 'top',
                            },
                            title: {
                                display: true,
                                text: 'WARRIORS PIE CHART'
                            }
                        }
                    }
                });
            })
            .catch(err => {
                console.log(err);
            });
    </script>
</body>
</html>