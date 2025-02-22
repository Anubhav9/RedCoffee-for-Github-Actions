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

### How to use RedCoffee for Github Actions ?

Using RedCoffee for Github Actions is very straight-forward. We just need to add the following block of code in the YAML file of our actions template. This is usually present in the .github/workflows directory.

```
- name: Use RedCoffee for Github Actions
  uses: Anubhav9/redcoffee-for-github-actions@v1.2
```

Please replace v1.2 with the version that you intend to use.

## How do we see the generated reports

The generated PDF report would be available to you in the Github Actions Section of your repository. Once inside the Github Actions section, click on the name of the action that you have created. This is usually available in the left side panel. For me, I have named the action as RedCoffee Bot. Hence it is visible to me like this in the following format

![image](https://github.com/user-attachments/assets/981423f6-b2b1-42c3-acf8-929889143b98)

Once inside this, search for the commit message that you provided while creating the commit and click on it. For me, this is the below one

![image](https://github.com/user-attachments/assets/1e82de1e-0cf6-461b-8b24-c11163b51ef6)

Click on this and navigate to artifactory sections. The report would be present there as a .zip file

![image](https://github.com/user-attachments/assets/cc0ae35a-0d91-4e98-885b-6cd6b5472565)

Please unzip the file. The report would be present there in .pdf format




