# Postman API Automation Integration with Github Action #

The Repository is a demonstration for POC for integrating Postman tests with Github Actions . The tests are written in postman and executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch .You can also execute the project manually using workflow_dispatch . The project runs on a scheduled time wit the help of a cron job

The HTML report is archived and kept in artifact section for the team to download it . Along with that they can view the report directly from https://sushie0208.github.io/Phoenix_Inwarranty_Flow/ .

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Schema Validation
5. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs
3. Newman
4. Newman-Reporter-htmlextra
5. Github Actions
6. Github pages


## Github Pages ##
You can directly view the latest test report of postman Test on Github Page - https://sushie0208.github.io/Phoenix_Inwarranty_Flow/

## HTML Report ##
The report will be created in newman folder
![Postman Report](https://raw.githubusercontent.com/sushie0208/Phoenix_Inwarranty_Flow/static-content/newman-report.png)

## Project Structure ##
```
InWarrantyFlow
├─ Inwarranty-Flow Collection Copy.postman_collection.json #Collection File
└─ QA.postman_environment.json #Environment File
```

## How to run the Project ? ##
You can run the projct on your local system , for that 
1. Clone the project on local system : https://github.com/sushie0208/Phoenix_Inwarranty_Flow.git
2. Install Nodejs and npm from https://nodejs.org/en/download
3. Install newman using command -  ```npm install -g newman```
4. Install newman-reporter-htmlextra using command - ```npm install -g newman-reporter-htmlextra```
5. run the newman command
   
           ```newman run 'Inwarranty-Flow Collection Copy.postman_collection.json' \
             -e QA.postman_environment.json \
             -r cli,htmlextra
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html```
