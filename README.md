# RedCoffee for Github Actions

### What is RedCoffee?

RedCoffee is a CLI tool written in Python that help developers generate insightful SonarQube Code Analysis Report in PDF Format. Please note that this works on SonarQube Community Edition.

### My motivation behind building RedCoffee

Last year, while working on a collaborative side project, my team and I integrated SonarQube to track code quality. Since this was purely a learning-focused initiative, we decided to use the SonarQube Community Edition, which met our needs—except for a few major limitations:

i) There was no built-in way to share the analysis report.

ii) Our SonarQube instance was running locally in a Docker container.

iii) No actively maintained plugins were available to generate reports.

After some research, I found an old plugin that supported PDF reports, but it had not been updated since 2016. Seeing no viable solution, I decided to build RedCoffee, a CLI-based tool that allows users to generate a PDF report for any SonarQube analysis, specifically designed for teams using the Community Edition.

### Some more info about RedCoffee

[ Pypi Link ](https://pypi.org/project/redcoffee/)

[ Github Repository ](https://github.com/Anubhav9/RedCoffee)

### Why RedCoffee for Github Actions?

This initially came to me as feature request. Since a lot of teams use Github Actions as CI Pipeline, it made sense to integrate this within the Github Actions block. I wanted to send this PDF report as a Slack message as well,
however, this has been hit with a roadblock that I'm currently trying to solve.

## How do we see the generated reports

The generated PDF report would be available to you in the Github Actions Section of your repository. Once inside the Github Actions section, click on RedCoffee For Github Actions. There you will see the artifactory. Click on the artifactory
and it will a .zip file. Once unzipped, you will find the PDF Report.

