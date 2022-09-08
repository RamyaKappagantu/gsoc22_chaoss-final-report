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
2. Gone through CHAOSS metrics and understood the working groups better. Understanding the difference between standard and non-standard metrics.
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

### Questions and Observations:
1. Can data_collection_date in discourse_insights table be null? - No, a timestamp is maintained everytime data is collected.
2. augur_data.issue_message_ref table also contains data about augur_data.pull_request_message_ref so when data is collected regarding both issues and pull requests for discourse analysis worker, we need to separate the data from augur_data.issue_message_ref that are not pull requests in order to avoid redundancy.
3. While analysing augur_data.discourse_insights table where the messages are classified into various discourse acts, I got to observe that the discourse act for the same message is different across different dates in a year.
4. The data collected in augur_data.discourse_insights is not uniform across time. For example, I got to see data collected across different years(2019 - 2022) whereas after few days, I got to see only data collected in 2022.

### To-Do's:
1. While working on adding visualizations to machine learning workers using Dash Library, I would like to understand more about 'Data' Input type in Dash callbacks to see if we can directly send a SQL query to 'Data' input type instead of providing the raw SQL query in the code.
2. Add more visualizations to augur machine learning workers.
3. Work on improving the performance of the machine learning workers.
4. Continue contributing to CHAOSS.

### Pull Requests:
[Adding visualization to discourse analysis worker.](https://github.com/sandiego-rh/explorer/pull/150)

