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
    <title>Document</title>
</head>
<body>
    <div id="plot_div"></div>
    <script>
         dfd.read_csv("https://raw.githubusercontent.com/paravsalaniwal/T3Project/master/_notebooks/files/warriors.csv")
            .then(df => {
                var layout = {
                    title: 'WARRIORS CHART',
                    xaxis: {title: 'Date'},
                    yaxis: {title: 'Count'}
                };
                var new_df = df.set_index({ key: "Date" });
                new_df.plot("plot_div").line({ columns: ["AAPL.Open", "AAPL.High"], layout: layout});
            }).catch(err => {
                console.log(err);
            });
    </script>
</body>
</html>