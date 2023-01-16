# Hosting a Full-Stack Application

## I used the udagram project to be deployed.

- haven't hard-coded any environment variables but I added them to circleci and passed them through the code to the deployment environment using the following command in the deploy.sh file: 'eb setenv JWT_SECRET=$JWT SECRET POSTGRES_DB=$POSTGRES DB POSTGRES_HOST=$POSTGRES MOST POSTGRES_PASSWORD=$POSTGRES_PASSWORD POSTGRES USERNAME=$POSTGRES_USERNAME

- The configuration files are updated to set the environment variables to the project code, for example, setting the server port and the server url and the database port the database url, user, and password. it's in udagram-api/ src/config/config.ts.

- I added all the scripts inside the package.json file. I added the scripts for installation, build, test and deployment for both the backend and the frontend to automate all the steps.

7

8

- I added the screenshots of all the aws resources and environments.

- I linked the project in github to circleci and added the config.yml file of the circleci containing all the orbs and jobs for running the scripts automatically.

- For accessing the application please visit: http://udagram-frontend-ziad-amer.s3-website-us-east-1.amazonaws.com but please make sure you are using a browser that doesn't enforce CORS policy** or blocking the user of the EB avs URL by the S3 URL.

- For accessing my github repository which is linked to circleci, please visit: https://github.com/ziad-amer-1/deployment_process Udacity deployment


## pipeline process inside circleci. # Continuous integration:

14 First I added all the commands needed for installing and building the application in the package.json files i the frontend and the backend then called these scripts inside the package.json file of the main application.

15 I added the jobs inside circleci config.yml file for installing all the dependencies on both the frontend and backend of the application using the : npm install' command inside package.json files.


### Continuous Deployment:

- First I added all the commands needed deploying the application in the package.json files in the frontend and the backend then called these scripts inside the package.json file of the main application.

- I added the Elastic Beanstalk and aws in the circleci orbs for setting them up and installing them for the

deployment.

- I added the jobs inside circleci yml file for deploying the frontend and the backend just by calling the deploy scripts added to the main package.json file which correspondingly calls the deploy commands added to the package.json file of both the frontend and the backend.

- I linked my github application to the circleci and specified the branch of interest which is the main branch so circleci is only trigged if the code pushed to the main branch.


## ALL the screenshots for the EB and 53 and DB and circleci are added to the zip file and to the corresponding directories and I also added a video of the running application after being deployed.

## I also added the Architecture diagram inside the infrastructure folder and the pipeline diagram inside the pipeline process folder, showing all the relationships and the communication between the different services.