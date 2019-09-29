# Creating Pipelines

This topic describes how application developers can create pipelines and configure pipeline stages and jobs for applications.

## Prerequisites

Before creating a pipeline, you need to complete the application creation and the basic information configuration. For detailed steps, see [Creating Applications](../admin/managing_app#newapp).

## Configuring the Basic Information for an Pipeline

You can create a pipeline for your application by taking the following steps:

1. In the project list, click a project name to enter the project space.

2. In the left navigation bar, select **Development > Pipeline**.

3. Click **New Pipeline** and enter the basic configuration information for the pipeline in the **Basic Information** section:

   - **Application Name**: Select a application from the created applications list for which the pipeline will be created.

   - **Pipline Name**: Enter the name of the pipeline.

   - **Language/Version**: Select the language and version for developing the application.

   - **Tool**: Choose the dependency that the language depends on, such as Java depends on Maven.

   - **Git Repository**: This field is automatically filled in with the repository of the selected application.

   - **Triggering Mode**: Select how to trigger the pipeline to run:

     - **Automatic**: Run the pipeline when the specified GitLab repository branch changes.
     - **Manual**: Manually select the GitLab repository branch and run the pipeline.
     - **Scheduled**: Run the pipeline at the set time.

   - **Branch**: Select the GitLab repository branch that runs the pipeline when the **Triggering Mode** is set to **Automatic** or **Scheduled**.

   - **Triggering Time**: Select the specific time to run the pipeline when the **Triggering Mode** is set to **Scheduled**.

     .. image:: ../../media/create_pipeline.png

4. After completing the basic information configuration, click **Add Stage** in the **Stage** section to configure the stages and jobs of the pipeline.


## Configuring Stages and Jobs

You can configure the stages and jobs for the pipeline by taking the following steps:

1. Enter the **Stage Name**.

2. Click the **Add Job** button, select the job type, and enter the required parameters.

   - **Build**
     - Job Name: Enter the name of the build job.
     - Docker File Path: Enter the Dockerfile storage path, such as docker/Dockerfile, which is the project root path by default.
     - Docker Registry: Select the docker image repository.

   .. note:: The build job will check if *build.sh* exists. If yes, it will automatically execute *build.sh*; if not, it will judge whether *pom.xml* exists, and if it exists, the *mvn Clean package -U -DskipTests* command will be executed. When building with the custom *build.sh*, you need to set the storage location for build results, such as war/tar/jar/zip packages, to the *target* directory under the project root directory.

   - **Deploy**
     - Job Name: Enter the name of the deployment task.
     - Cluster: Select the cluster where the application will be deployed.
     - Resource Type: Select the resource type for the deploy job, where you can select Deployment or StatefulSet.
     - Resource Name: Select the deployment configuration name of the application. See [Configuring Deployments](../container/configuring_deployment) for more information.

   - **Scan**
     - Job Name: Enter the name of the code scanning job.
     - Source Code: Enter the path to the file to be scanned, such as *src/main/java*, *src/main/java/utils/Test.java*.
     - Exclusion Files: Enter file paths that do not need to be scanned, such as src/main/java/*, src/main/java/**/, src/main/java/utils/Test.java.
     - Unit Test: Select whether to perform unit test. If yes, enter the path of the test file, such as *src/test*.

   .. note:: The code scanning job will check if *build.sh* exists. If yes, it will automatically execute *build.sh*; if not, it will judge whether *pom.xml* exists, and if it exists, the *mvn clean compile -DskipTests* command will be executed. When Java is used as the programming language, it will check whether there is a *sonar-project.properties* file. If yes, *sonar-scanner* will be used to complete the code scanning, and if not, *mvn sonar:sonar* will be used. As for other programming languages such as Node.js, *sonar-scanner* will be used for code scanning by default.

   - **Publish Dependency**
     - Job Name: Enter the job name.
     - Build Path: Enter the path where the pom file is located, such as *share*, which is the project root path by default.
     - Parameters: The default command for Java is *mvn deploy*, and you can add parameters like *-DskipTests*. The default command for npm is *npm publish*, and you can add parameters like *--access=public*.

   - **Jenkins Job**
     - Job Name: Enter the name of the Jenkins job.
     - Jenkins URL: Enter the Jenkins service address, eg: <http://jenkins-ci.envisioncn.com:8080/jenkins>.
     - Username: Enter the Jenkins username.
     - API Token: Enter the API Token generated by the Jenkins username.
     - Job Name: Enter the Jenkins job name.
     - Parameters: Enter the required Jenkins parameters.

   - **Custom Job**
     - Job Name: Enter the name of the custom job.
     - Shell Script Path: Enter the path of the script file that you want to run.

3. Click and drag the task to sort the running order of the jobs.

   .. image:: ../../media/add_stage.png

4. After the job configuration required in the stage is completed, click **Add Stage** and repeat the above-mentioned steps to add the second stage of the pipeline.

5. After the stage configuration is completed, click the **New Pipeline** button to save the pipeline configuration.

## Next Step

Once the pipeline is created, you can run the pipeline and view the pipeline running status and results.

<!--end-->
