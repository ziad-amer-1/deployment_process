### The Application itself:

- First I added all the commands needed for installing, testing and building the application in the package.json files in the frontend and the backend then called these scripts inside the package.json file of the main application.

- I added the jobs inside circleci config.yml file for installing all the dependencies on both the frontend and backend of the application using the: npm install command inside package.json files.


> - Then I added the jobs for building the frontend and the backend by calling the corresponding scripts.

### AMS Deployment:

- RDS Postgres database instance that has the database structure with all the data content and is linked to backend code (inside Elastic Beanstalk)

- Elastic Beanstalk environment that handles the application environment and sends requests to RDS database and
receives the response to be sent to the frontend inside S3 to display the relevant webpages to the user.

- 53 that holds the frontend files which also sends the requests to the backend to be handeled and renders the HTML pages returned as a response to be displayed to the user.

### The Architecture Diagram is added showing the communication between these different services and infrastructure.
### The screenshots of the instances created in the aws services are added to the infrastructure directory as well.