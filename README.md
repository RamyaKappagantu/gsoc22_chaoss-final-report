# GSoC'22 Project Final Report
## Machine Learning Based Community Health and Communication
### Project Summary:
Augur is a Python library, REST server and Flask web application which is used to collect free and open source data and provide meaningful insights around it. The data is collected across various sources like open source repos, mailing lists and other communication systems. Augur uses categorised workers to collect specific data. Currently CHAOSS provides metrics by dividing them into working groups. Few of such metrics are frequency of contributions, types of contributions, time frame between opening and closing a pull request, diversity and inclusion, leadership, efficiency and effectiveness of mentorship programs. This project will play an important role in analysing the open source community health. It provides an efficient way to compute and visualise the metrics through an API. Using this API will provide a more accessible way to understand and visualise various metrics. 
### Deliverables: 
1. Create an API for visualising the metrics provided by various machine learning workers and improve their performance. 
2. Work on implementing new metrics within the augur machine learning workers and test the performance of newly added metrics with the optimised model to see if the optimised model works for new metrics added. 
3. Work on augur_view to provide a customised and accessible dashboard to the user.

### Community Bonding and Coding Phase 1:
1. Gone through the Augur Database Schemas to understand the augur workers dependencies.
2. Gone through CHAOSS metrics and understood the working groups better.
3. Understood SQL Alchemy better and the advantages of SQL Alchemy over SQL or standard database model.
4. Setting up augur environment to run the visualizations.
5. Understood pull_request_reports.py and contributors_reports.py to develop a workflow for generating new visualizations for augur workers.
6. Understood machine learning workers and it's dependencies required for the project: Discourse Analysis, Message Insights, Pull Request Analysis and Clustering worker.
7. Started working on adding visualizations to discourse analysis worker and developed a python script using bokeh library to create a visualization which counts the pull requests and issues per discourse act.
8. Got to learn about Sandiego Project which uses a web app to generate visualizations using Dash library.
9. Understood the workflow of the Sandiego Project web app and also explored more about Dash library.
10. Worked on setting up the environment for Sandiego Project web app by building the container.
11. Started working on enhancing the previously developed visualizations using Dash library.

### Coding Phase 2:
1. Continued working on developing the visualizations for discourse analysis worker using Dash Library.
2. Worked on enhancing the performance of the code by improving the underlying SQL query.
3. Thought of 2 workflows to see which performs the best: 
    a.  Computing the discourse counts within the python script.
    b.  Computing the discourse counts within the PostgreSQL query and using it within the python script.
