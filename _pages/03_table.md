---
layout: page
title: Testing JS W Pandas
permalink: /Tester/
---



<script>

 // Assuming you have included the required dependencies

// Read the CSV file
const data = pd.read_csv('/notebooks/files/wizards.csv');

// Convert the DataFrame to HTML
const htmlTable = data.to_html({ index: false });

// Display the HTML table
display(HTML(htmlTable));

</script>