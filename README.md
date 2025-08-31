# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating Postman tests with github actions.The Tests are written in postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch.You can also execute the project manually using workflow-dispatch.The Project runs on a schedule time with the help of the cron job.

The HTML report is archived and kept in the artifact section for the team to download it.Along with that they can view the report directly from the github page : https://gargpriya01.github.io/Phoenix-Inwarranty-flow/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi, My name is Priya Garg.I have 9 years of experience in Automation Testing.My skillset includes UI Automation with Selenium WebDriver, and for API automation I use Rest Assured and you can connect with me over: https://www.linkedin.com/in/priya-garg01/


## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node.js 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS EC2 instance for Self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link : https://gargpriya01.github.io/Phoenix-Inwarranty-flow/

## HTML Extra ##
The Report will be created in the newman folder
![Postman Report](https://github.com/gargpriya01/Phoenix-Inwarranty-flow/blob/static-content/newman-report.png)

## Project Structure ##

```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json  #Collection file
├─ QA.postman_environment.json  #Environment file
└─ testdata.csv  #Test Data file

```

## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on Local system : ```https://github.com/gargpriya01/Phoenix-Inwarranty-flow.git```
2. Install Node.js and NPM from ```https://nodejs.org/en```
3. Install Newman using ```npm install -g newman```
4. Install Newman-reporter-htmlextra ```npm install -g newman-reporter-htmlextra```
5. Run the Newman command:
```
           newman run 'Inwarranty-flow Collection.postman_collection.json' \
           -e QA.postman_environment.json \
           - d testdata.csv \
           -r cli,htmlextra \
           --reporter-htmlextra-export ./newman/index.html
```




