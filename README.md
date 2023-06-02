Petite Pandas group - Data Analysis with Pandas and NumPy

Uses a Python backend with a HTML/Javascript frontend in order to create our NBA stats project.

Backend:
- Individual CSV files are made and referenced
- Pandas are used to extract all the data from the csv files and compiles them into one giant JSON file
- The JSON file contains separate dictionaries for each team, and multiple lists and dictionaries are present within
- Pandas are also used in the code that helps set up the graphs with the axis and the different aspects
- The backend also generates tables for each team

Frontend:
- Consist of 3 dropdown menus: 1 for table, 1 for bar graph, and 1 for pie graph
- The  choices for the table have the teams, while the choices for the graphs include aspects like points and steals
- When a specific team is clicked, the table with the data for that team is generated
- Once the table is generated, users can then click on one of the choices for the graphs, and the graph for that aspect within the team will show up
