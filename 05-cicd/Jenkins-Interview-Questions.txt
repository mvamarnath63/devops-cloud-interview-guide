Jenkins interview question and answers for  BEGINER LEVEL
1. What is Jenkins?
Jenkins is an open-source automation tool that helps in continuous integration and continuous delivery (CI/CD) of software projects. It automates the building, testing, and deployment of applications, allowing developers to integrate their code changes frequently and detect issues early in the development process.

​

2. How does Jenkins work?
Jenkins works by allowing users to create jobs that perform specific tasks. These jobs are configured to trigger automatically based on certain events, such as code commits, time schedules, or manual triggers. Jenkins pulls the latest code changes from the version control system, builds the project, runs tests, and deploys the application if all checks pass.

 

3. What are the key features of Jenkins?
Some key features of Jenkins include:
- Continuous integration and continuous delivery (CI/CD) capabilities
- Extensibility through a large number of plugins
- Distributed builds and support for parallel execution
- Easy installation and configuration
- Robust error handling and notifications
- Support for various version control systems and build tools
- Detailed reports and logs for better visibility into the build process

 

4. How can you install Jenkins?
To install Jenkins, you can follow these steps:
- Download the Jenkins WAR file from the official Jenkins website.
- Install Java on your system if it's not already installed.
- Open a terminal or command prompt and navigate to the directory where the Jenkins WAR file is located.
- Run the command: `java -jar jenkins.war`
- Jenkins will start and can be accessed through a web browser using the URL: `http://localhost:8080`

 

5. What are Jenkins plugins?
Jenkins plugins are extensions that enhance the functionality of Jenkins. They allow you to add new features, integrate with third-party tools, and customize the behavior of Jenkins. There is a wide range of plugins available for different purposes, such as source code management, build tools, testing frameworks, deployment, and more.

 

6. How do you create a Jenkins job?
To create a Jenkins job, follow these steps:
- Log in to Jenkins and click on "New Item" on the Jenkins dashboard.
- Enter a name for your job and select the type of job you want to create (freestyle project, pipeline, etc.).
- Configure the job by providing necessary details like source code repository, build steps, test commands, post-build actions, and notifications.
- Save the job configuration, and Jenkins will start executing it based on the triggers you have set.

 

7. What is a Jenkins pipeline?
A Jenkins pipeline is a way to define and manage the entire CI/CD process in code. It allows you to define the stages, steps, and conditions for your build, test, and deployment processes using a Jenkinsfile, which is written in Groovy. Pipelines provide better visibility, reusability, and version control for your CI/CD workflows.

 

8. How do you define a Jenkins pipeline?
To define a Jenkins pipeline, you need to create a Jenkinsfile in the root directory of your project. The Jenkinsfile contains the script that defines the pipeline stages and steps. You can define the pipeline using either the declarative syntax or the scripted syntax, depending on your preference and requirements.

 

9. What are Jenkins agents?
Jenkins agents (formerly known as slaves) are machines that are connected to the Jenkins master and execute the build and deployment tasks. Agents can be distributed across different machines, allowing parallel execution of jobs and scaling the build capacity. They communicate with the Jenkins master to receive instructions and report the build status.

 

10. How can you secure Jenkins?
To secure Jenkins, you can take the following measures:
- Enable security and authentication by configuring user accounts and access controls.
-

 Use HTTPS with SSL/TLS encryption for secure communication.
- Regularly update Jenkins to the latest stable version to get security patches and bug fixes.
- Use plugins like the Role-Based Access Control plugin to fine-tune user permissions.
- Disable or restrict access to Jenkins administration features for non-administrative users.
- Follow best practices for securing the underlying server infrastructure hosting Jenkins.

​

Jenkins interview question and answers for  INTERMEDIATE LEVEL
1. What is a Jenkinsfile, and how is it different from traditional job configurations?
A Jenkinsfile is a text file that contains the definition of a Jenkins pipeline. It allows you to define the entire CI/CD process as code, including stages, steps, and conditions. The Jenkinsfile can be stored in version control along with your source code, providing better traceability and versioning compared to traditional job configurations stored within Jenkins.

 

2. What is the difference between scripted and declarative pipelines in Jenkins?
Scripted pipelines in Jenkins use a Groovy-based scripting syntax to define the CI/CD process. They offer more flexibility and fine-grained control over the pipeline flow but can be more complex to write and maintain. Declarative pipelines, on the other hand, use a simpler and more structured syntax. They provide a predefined structure for pipeline stages and enforce best practices, making them easier to read, understand, and maintain.

 

3. How do you handle Jenkins pipeline failures and retries?
In Jenkins pipelines, you can handle failures and retries using error handling and exception handling techniques. For example, you can use the `catch` block to catch specific exceptions and define appropriate actions, such as sending notifications, retrying a failed stage, or marking the build as unstable or failed based on certain conditions.

 

4. How can you parameterize Jenkins jobs to make them more flexible?
Jenkins allows you to parameterize your jobs, which enables you to provide inputs or options when triggering the job. You can add parameters such as strings, Boolean values, choice parameters, or even file uploads. This makes the job more flexible and reusable as it can be configured differently each time it is triggered.

 

5. Explain the concept of Jenkins distributed builds and how they can be set up.
Jenkins distributed builds allow you to distribute the execution of jobs across multiple machines, known as Jenkins agents. This enables parallel execution of jobs and improves overall build capacity. To set up distributed builds, you need to configure Jenkins agents and connect them to the Jenkins master. Agents can be set up on different physical or virtual machines and can be dedicated or shared among multiple projects.

 

6. What are Jenkins pipelines' best practices for efficient and maintainable CI/CD workflows?
Some best practices for Jenkins pipelines include:
- Keeping pipelines modular and reusable by using shared libraries and functions.
- Using proper error handling and notifications for failed builds.
- Following the "Single Responsibility Principle" and keeping pipelines focused on specific tasks.
- Utilizing parallel stages and agents for faster builds.
- Using version control for Jenkinsfiles and regularly reviewing and updating them.
- Using code linters and static analysis tools to ensure pipeline code quality.

 

7. How can you integrate Jenkins with external tools or services?
Jenkins provides a wide range of plugins to integrate with various external tools and services. Some common integrations include:
- Version control systems (e.g., Git, SVN)
- Build tools (e.g., Maven, Gradle)
- Testing frameworks (e.g., JUnit, Selenium)
- Artifact repositories (e.g., Nexus, Artifactory)
- Deployment and orchestration tools (e.g., Ansible, Kubernetes)
- Notification services (e.g., Slack, email)

 

8. How can you achieve high availability and scalability in a Jenkins setup?
To achieve high availability and scalability in a Jenkins setup, you can:
- Set up a Jenkins master with multiple agents in a distributed configuration.
- Use load balancers to distribute incoming requests across multiple Jenkins masters.
- Employ cloud-based infrastructure to dynamically scale agents based on demand.
- Implement Jenkins master-slave setups for redundancy.
- Regularly back up and restore Jenkins data to prevent data loss.

​

​

Jenkins interview question and answers for ADVANCED LEVEL
1. What is Jenkins Pipeline Shared Library, and how do you use it?
Jenkins Pipeline Shared Library allows you to define reusable code and functions that can be shared across multiple pipelines. It enables you to centralize common pipeline logic, promote code reuse, and maintain consistency across projects. To use a Shared Library, you define it in a separate repository, configure Jenkins to load the library, and then use the library functions in your Jenkins pipelines.

 

2. Explain the concept of Jenkins Agents in Kubernetes (Jenkins Kubernetes Plugin).
Jenkins Kubernetes Plugin allows you to dynamically provision Jenkins agents on Kubernetes clusters. Agents are created as pods in the Kubernetes cluster and are automatically scaled up or down based on the workload. This integration provides better scalability, resource utilization, and isolation for Jenkins builds, especially in cloud or containerized environments.

 

3. How can you implement Jenkins pipeline parallelization and what are the considerations?
Parallelization in Jenkins pipelines allows you to execute multiple stages or steps concurrently, reducing the overall build time. To implement parallelization, you can use the `parallel` step in a Jenkins pipeline and define multiple branches or stages to execute in parallel. Considerations include ensuring proper synchronization points, managing resource usage, handling dependencies between parallel branches, and monitoring and reporting the progress of parallel executions.

 

4. What are Jenkins pipeline stages and how can you control their execution?
Stages in Jenkins pipelines represent distinct phases of the CI/CD process, such as build, test, deploy, and so on. Stages provide a structured way to visualize and control the pipeline flow. You can define stages using the `stage` directive in a Jenkinsfile and configure their execution order. Additionally, you can use conditions, like `when` or input parameters, to control whether a stage should be executed or skipped based on specific criteria.

 

5. How do you implement Jenkins pipeline testing and quality gates?
Jenkins pipeline testing involves running various types of tests, such as unit tests, integration tests, and acceptance tests, as part of the pipeline. You can integrate testing frameworks and tools into the pipeline and define stages or steps for running tests. Quality gates can be implemented using conditions or thresholds on test results, code coverage, static code analysis, or other metrics. If the defined criteria are not met, the pipeline can be marked as failed or unstable.

 

6. What is Blue Ocean in Jenkins, and how does it enhance the user interface?
Blue Ocean is a plugin for Jenkins that provides a modern, intuitive, and user-friendly interface for visualizing and managing Jenkins pipelines. It offers a more streamlined and graphical representation of pipelines, with a visual editor for creating and modifying pipelines. Blue Ocean enhances the user experience by providing better visualization, easier navigation, and improved pipeline status tracking.

 

7. How can you secure sensitive information, such as credentials, in Jenkins pipelines?
Jenkins provides the Credentials plugin to securely manage sensitive information in pipelines. You can store credentials, such as usernames, passwords, or SSH keys, in Jenkins' credential store and access them in your pipeline using the appropriate credential bindings. Avoid hardcoding or exposing sensitive information in the pipeline script itself, and ensure proper access controls are in place to restrict access to sensitive credentials.

 

8. Explain the concept of Jenkins pipeline as code and its benefits.
Jenkins pipeline as code refers to defining and managing the Jenkins pipeline configuration and logic as code, typically using a Jenkinsfile. The benefits include version control and traceability of pipeline changes, better collaboration and code review processes, automation of the entire CI/CD process, improved reusability and modularity, easier maintenance and troubleshooting, and the ability to leverage software development best practices for the pipeline code.

 

​

Jenkins interview question and answers SCENARIO BASED
Scenario 1:
You have a Jenkins pipeline that deploys a web application to multiple environments: Development, Staging, and Production. Each environment requires different deployment configurations. How would you implement this in Jenkins?

Answer:
To implement this in Jenkins, you can define a parameterized pipeline job that takes an input parameter for the target environment. Based on the provided environment parameter, you can use conditional statements within the pipeline to execute the corresponding deployment configurations. For example, you can use a `switch` statement to determine which set of deployment configurations to use for each environment.

 

Scenario 2:
You have a Jenkins pipeline that builds and tests your application code. However, the testing process takes a long time to complete, and you want to speed it up by running tests in parallel. How would you achieve this in Jenkins?

Answer:
To speed up testing by running tests in parallel, you can use the `parallel` step in Jenkins pipelines. You can split your tests into multiple test suites or categories and create separate stages or branches within the `parallel` step. Each branch can run a subset of tests concurrently, utilizing multiple agents or executor slots. This allows you to distribute the test workload and significantly reduce the overall testing time.

 

Scenario 3:
You want to implement an approval process in your Jenkins pipeline before deploying to production. The deployment should proceed only if it receives approval from a designated user or team. How can you achieve this in Jenkins?

Answer:
To implement an approval process in Jenkins pipelines, you can use the `input` step. Place the `input` step in a specific stage of your pipeline, typically before the production deployment stage. This step will pause the pipeline and prompt the designated user or team to provide approval. Once the approval is granted, the pipeline will resume and proceed with the production deployment. You can customize the input message and add a timeout for automatic rejection if no response is received within a specified period.

 

Scenario 4:
You have a Jenkins pipeline that triggers builds automatically whenever changes are pushed to the Git repository. However, you want to add an additional condition to only trigger a build if changes are made to specific directories within the repository. How would you achieve this in Jenkins?

Answer:
To trigger a build only when changes are made to specific directories in a Git repository, you can utilize the Jenkins Git plugin and the "Poll SCM" feature. In the job configuration, enable the "Poll SCM" option and provide a schedule to periodically check for changes. Additionally, you can specify the directories to include or exclude using the "Included Regions" or "Excluded Regions" field in the Git configuration. This way, Jenkins will trigger a build only if changes occur within the specified directories.

 

Scenario 5:
You have a Jenkins pipeline that deploys Docker containers to a Kubernetes cluster. You want to ensure that the deployment rolls back to the previous version if any issues are detected during the rollout. How would you implement this in Jenkins?

Answer:
To implement automated rollback in a Jenkins pipeline for Kubernetes deployments, you can use the Kubernetes plugin and the Kubernetes Deployment object's rollback feature. Within your pipeline, you can capture the current deployment version before initiating the deployment. Once the deployment is complete, you can monitor for any issues by performing health checks. If issues are detected, you can trigger the rollback by using the Kubernetes plugin's `kubectlRollback` step, specifying the deployment and the previous version to roll back to.

Remember, 

​

Scenario 6:

You have a Jenkins pipeline job that builds and deploys your application. You want to trigger this job automatically whenever changes are pushed to a specific branch in your Git repository. How can you achieve this?
Answer: You can set up a webhook in your Git repository that sends a notification to Jenkins whenever changes are pushed to the specified branch. In Jenkins, you can create a pipeline job and configure it to listen to the webhook trigger. Whenever the webhook is triggered, Jenkins will automatically start the pipeline job to build and deploy your application.
Scenario: You have multiple Jenkins jobs that need to share some common environment variables or configurations. How would you manage these shared configurations efficiently?
Answer: Jenkins provides the concept of global environment variables that can be shared across multiple jobs. You can define these variables in the Jenkins global configuration settings. Once defined, they can be accessed by any Jenkins job, making it easier to manage and update shared configurations.
 

Scenario 7:

You have a Jenkins job that builds and tests your application. You want to schedule this job to run at a specific time every day, even on weekends. How can you schedule the job accordingly?
Answer: In Jenkins, you can use the "Build periodically" option to schedule a job to run at specific times. To run the job every day, including weekends, you can use the cron syntax. For example, setting the schedule to "0 9 * * *" will run the job every day at 9:00 AM.
 

Scenario 8:

You have a Jenkins pipeline that deploys your application to multiple environments, such as development, staging, and production. However, you want to restrict the deployment to production only when a specific approval step is completed. How can you implement this approval process in your pipeline?
Answer: In Jenkins, you can use the "input" step in your pipeline to prompt for manual approval. After the deployment to the staging environment, you can add an input step that waits for approval. Once the approval is provided, the pipeline can continue and deploy the application to the production environment.
 

Scenario 9: You have a Jenkins job that builds and packages your application into a Docker container. After building the container, you want to publish it to a Docker registry. How can you achieve this?
Answer: Jenkins provides various plugins for Docker integration. You can use plugins like "Docker Plugin" or "Docker Pipeline" to push the Docker container to a Docker registry. These plugins allow you to specify the registry credentials, image name, and other configuration details within your Jenkins job.

 

Scenario10:

You have a Jenkins pipeline job that builds and deploys your application. You want to automatically trigger the pipeline whenever changes are pushed to a specific branch, but you also want to include a manual approval step before deploying to production. How can you achieve this?
Answer: You can set up a webhook in your Git repository to trigger the Jenkins pipeline whenever changes are pushed to the specified branch. Within the pipeline, you can include a stage with an "input" step that waits for manual approval before deploying to production. Once the approval is given, the pipeline will continue with the deployment.

 

Scenario11:

You have a Jenkins job that builds and tests your application, and you want to automatically trigger the job whenever changes are pushed to any branch except the "master" branch. How can you configure this in Jenkins?
Answer: In Jenkins, you can set up a multi-branch pipeline job that automatically detects and builds branches in your Git repository. By default, it builds all branches, but you can exclude specific branches by using the "Branch Sources" configuration and specifying a regular expression pattern to exclude the "master" branch. This way, the job will be triggered for changes in any other branch except the "master" branch.

 

Scenario12:

You have a Jenkins pipeline job that builds and deploys your application to multiple environments, such as development, staging, and production. However, you want to skip the deployment to the production environment during non-working hours. How can you achieve this?
Answer: Within your Jenkins pipeline, you can include conditional logic to check the current time. You can use a script step to evaluate the time and based on the result, decide whether to proceed with the deployment to the production environment or skip it. This way, you can skip the production deployment during non-working hours.

 

Scenario13: You have a Jenkins job that builds your application and creates an artifact, and you want to store and manage these artifacts for future use. How can you configure Jenkins to manage artifacts?
Answer: Jenkins provides a built-in feature called "Artifacts" that allows you to archive and manage build artifacts. In your Jenkins job configuration, you can specify the files or directories to be archived as artifacts. Once the job completes, the artifacts will be stored and can be accessed through the Jenkins UI. You can also configure retention policies to control how long the artifacts should be kept.

 

Scenario14: You want to monitor the health and performance of your Jenkins pipelines and jobs. How can you achieve this?
Answer: Jenkins provides various plugins and integrations for monitoring and performance tracking. Plugins like "Metrics" and "Monitoring" offer metrics and visualization options to monitor the health and performance of Jenkins. Additionally, Jenkins supports integrations with external monitoring systems like Prometheus and Grafana, which provide advanced monitoring capabilities. By configuring these plugins and integrations, you can monitor and analyze the health and performance of your pipelines and jobs

 

Scenario15:

You have a Jenkins pipeline that deploys your application to multiple environments, and you want to automatically rollback to the previous deployment if the current deployment fails. How can you achieve this?
Answer: Within your Jenkins pipeline, you can use a try-catch block to catch any errors that occur during the deployment process. In the catch block, you can implement the rollback logic to revert to the previous deployment. Here's an example of how the script could look like:
pipeline {
    stages {
        stage('Deploy') {
            steps {
                script {
                    try {
                        // Deployment logic
                        deployToEnvironment('production')
                    } catch (Exception e) {
                        // Rollback logic
                        rollbackToPreviousDeployment('production')
                    }
                }
            }
        }
    }
}

def deployToEnvironment(environment) {
    // Deployment code specific to the environment
    // ...
}

def rollbackToPreviousDeployment(environment) {
    // Rollback code specific to the environment
    // ...
}

 

Scenario16:

You have a Jenkins job that builds and packages your application into multiple artifacts, and you want to archive and publish these artifacts to an artifact repository for future use. How can you achieve this?
Answer: Within your Jenkins job, you can use the archiveArtifacts step to specify the files or directories to be archived as artifacts. After archiving, you can use plugins like "Artifactory" or "Nexus Artifact Uploader" to publish the artifacts to an artifact repository. Here's an example of how the script could look like:
pipeline {
    stages {
        stage('Build') {
            steps {
                // Build and package your application
                // ...
                
                // Archive the artifacts
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }
        stage('Publish') {
            steps {
                // Publish artifacts to the artifact repository
                publishArtifactsToRepository()
            }
        }
    }
}

def publishArtifactsToRepository() {
    // Publishing logic using the artifact repository plugin
    // ...
}

 

Scenario17:

You have a Jenkins pipeline that builds and tests your application, and you want to trigger additional actions, such as sending a notification or executing a script, only when the build or test fails. How can you achieve this?
Answer: Within your Jenkins pipeline, you can use the post section to define post-build actions that should be executed based on the build result. You can use the failure condition to specify actions that should only run when the build fails. Here's an example of how the script could look like:
pipeline {
    stages {
        stage('Build') {
            steps {
                // Build your application
                // ...
            }
        }
        stage('Test') {
            steps {
                // Test your application
                // ...
            }
        }
    }
    
    post {
        failure {
            // Actions to perform when the build or test fails
            sendNotification()
            executeScript()
        }
    }
}

def sendNotification() {
    // Notification logic
    // ...
}

def executeScript() {
    // Script execution logic
    // ...
}

 

Scenario18:

You have a Jenkins pipeline that builds and tests your application, and you want to parallelize the test execution to reduce the overall testing time. How can you achieve parallel test execution?
Answer: Within your Jenkins pipeline, you can use the parallel step to define parallel stages for test execution. Each stage can represent a different subset of tests or a different test category. Here's an example of how the script could look like:
pipeline {
    stages {
        stage('Build') {
            steps {
                // Build your application
                // ...
            }
        }
        stage('Test') {
            steps {
                // Parallel test execution
                parallel(
                    "Unit Tests": {
                        // Execute unit tests
                        // ...
                    },
                    "Integration Tests": {
                        // Execute integration tests
                        // ...
                    },
                    "End-to-End Tests": {
                        // Execute end-to-end tests
                        // ...
                    }
                )
            }
        }
    }
}
 

Scenario19:

You want to implement an automated release process in Jenkins, where the pipeline automatically creates a release branch, performs versioning, builds artifacts, generates release notes, and deploys to production. How can you achieve this?
Answer: To implement an automated release process in Jenkins, you can leverage plugins like "Git Plugin" and "Semantic Versioning Plugin" along with custom scripting. Here's an example of how the script could look like:
pipeline {
    stages {
        stage('Prepare Release') {
            steps {
                // Create a release branch from the main branch
                createReleaseBranch()
                
                // Update the version number using semantic versioning
                updateVersionNumber()
            }
        }
        stage('Build & Package') {
            steps {
                // Build and package your application
                // ...
            }
        }
        stage('Generate Release Notes') {
            steps {
                // Generate release notes based on commits
                generateReleaseNotes()
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the release artifacts to the production environment
                deployToEnvironment('production')
            }
        }
    }
}

def createReleaseBranch() {
    // Create a release branch from the main branch
    // ...
}

def updateVersionNumber() {
    // Update the version number using semantic versioning
    // ...
}

def generateReleaseNotes() {
    // Generate release notes based on commits
    // ...
}

def deployToEnvironment(environment) {
    // Deployment code specific to the environment
    // ...
}

​

Jenkins Commands
NOTE:  replace `http://localhost:8080/` with the actual URL of your Jenkins server.

1. `java -jar jenkins.war` - Starts Jenkins server.
2. `jenkins-cli.jar -s http://localhost:8080/ help` - Retrieves the help information.
3. `java -jar jenkins-cli.jar -s http://localhost:8080/ version` - Checks the Jenkins version.
4. `java -jar jenkins-cli.jar -s http://localhost:8080/ list-jobs` - Lists all jobs on the Jenkins server.
5. `java -jar jenkins-cli.jar -s http://localhost:8080/ create-job myjob < config.xml` - Creates a new job named "myjob" using the provided XML configuration.
6. `java -jar jenkins-cli.jar -s http://localhost:8080/ delete-job myjob` - Deletes the "myjob" job.
7. `java -jar jenkins-cli.jar -s http://localhost:8080/ build myjob` - Triggers a build for the "myjob" job.
8. `java -jar jenkins-cli.jar -s http://localhost:8080/ safe-restart` - Performs a safe restart of the Jenkins server.
9. `java -jar jenkins-cli.jar -s http://localhost:8080/ safe-shutdown` - Performs a safe shutdown of the Jenkins server.
10. `java -jar jenkins-cli.jar -s http://localhost:8080/ cancel-quiet-down` - Cancels the quiet-down mode.
11. `java -jar jenkins-cli.jar -s http://localhost:8080/ quiet-down` - Puts Jenkins into a quiet-down mode, allowing all running builds to complete.
12. `java -jar jenkins-cli.jar -s http://localhost:8080/ disable-job myjob` - Disables the "myjob" job.
13. `java -jar jenkins-cli.jar -s http://localhost:8080/ enable-job myjob` - Enables the "myjob" job.
14. `java -jar jenkins-cli.jar -s http://localhost:8080/ get-job myjob` - Retrieves the XML configuration of the "myjob" job.
15. `java -jar jenkins-cli.jar -s http://localhost:8080/ reload-configuration` - Reloads the Jenkins configuration from disk.
16. `java -jar jenkins-cli.jar -s http://localhost:8080/ clear-queue` - Clears the build queue.
17. `java -jar jenkins-cli.jar -s http://localhost:8080/ create-node mynode` - Creates a new Jenkins node named "mynode".
18. `java -jar jenkins-cli.jar -s http://localhost:8080/ delete-node mynode` - Deletes the Jenkins node named "mynode".
19. `java -jar jenkins-cli.jar -s http://localhost:8080/ list-changes myjob` - Lists the SCM changes for the "myjob" job.
20. `java -jar jenkins-cli.jar -s http://localhost:8080/ copy-job myjob newjob` - Copies the "myjob" job and creates a new job named "newjob".
21. `java -jar jenkins-cli.jar -s http://localhost:8080/ set-build-description myjob 42 "Build successful"` - Sets the build description for build number 42 of the "myjob" job.
22. `java -jar jenkins-cli.jar -s http://localhost:8080/ get-builds myjob` - Lists all builds of the "myjob" job

.
23. `java -jar jenkins-cli.jar -s http://localhost:8080/ delete-builds myjob 1-10` - Deletes builds 1 to 10 of the "myjob" job.
24. `java -jar jenkins-cli.jar -s http://localhost:8080/ copy-builds myjob 42 newjob` - Copies build number 42 of the "myjob" job to the "newjob" job.
25. `java -jar jenkins-cli.jar -s http://localhost:8080/ set-build-result myjob 42 FAILURE` - Sets the result of build number 42 of the "myjob" job to FAILURE.
26. `java -jar jenkins-cli.jar -s http://localhost:8080/ clear-build-result myjob 42` - Clears the result of build number 42 of the "myjob" job.
27. `java -jar jenkins-cli.jar -s http://localhost:8080/ tail-log myjob` - Displays the console output log for the "myjob" job.
28. `java -jar jenkins-cli.jar -s http://localhost:8080/ cancel-build myjob 42` - Cancels build number 42 of the "myjob" job.
29. `java -jar jenkins-cli.jar -s http://localhost:8080/ set-next-build-number myjob 100` - Sets the next build number of the "myjob" job to 100.
30. `java -jar jenkins-cli.jar -s http://localhost:8080/ who-am-i` - Displays information about the current user.

​