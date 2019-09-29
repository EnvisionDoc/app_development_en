# Get Started

This article helps you quickly build and deploy an application, publish the application to a specified cluster, and test the application by using EnOS SHC.

## About the Scenario

An application named *uic* for querying personnel information in the organization has been developed. The source code of the application is stored in GitLab. Publish the application to the *beta* cluster with EnOS SHC, and then test using the application to query personnel information.

## About this Task

In an application development project, complete container configuration for the application *uic*, create a pipeline for the application, and then publish it online. Detailed steps include configuring deployment, service, and route for the application, creating a pipeline with build, code scanning, and deployment tasks, and running the pipeline. When all the steps are completed, use the application to query personnel information.

Based on the above requirements, the process of quickly publishing an application is shown in the following figure:

.. image:: media/app_deployment_process_e.png

## Prerequisites

1. An application development project has been created in EnOS SHC. An application named *uic* has been created, and the application code has been stored in GitLab repository.
2. You are a member of the application development project and have development permission for the application *uic*. For more information about role and permission, see [Managing Projects and Applications](../howto/admin/index.html).

## Step 1: Configure Deployment

In this step, create deployment configuration for the application *uic* and complete the detailed resource configuration for the application deployment.

1. Log in the EnOS Console and select **Service Hosting Center** in the left navigation panel to enter the application development project page.

2. In the left navigation bar, select **Container > Deployments**.

3. Click **New Deployment**, select **Config** mode, and provide the following deployment configuration information:

   - Application Name: uic
   - Environment: beta
   - Cluster: beta-k8s-cn4
   - Replicas: 1
   - CPU Minimum: 0.1; CPU Maximum: 0.8
   - Memory Minimum: 0.1; Memory Maximum: 0.5
   - Readiness Probe: On
   - Timeout: 120
   - Period: 2
   - Retry Times: 3             
   - Initial Delay: 20
   - Handler: tcpSocket; TCP Port: 8080
   - Minimum Readiness Time: 30s
   - Description: Deployment configuration for application *uic* in beta environment 

4. Click the **New Deployment** button to save the deployment configuration.

   .. image:: media/deployment1_2.png


## Step 2: Configure Config Map and Update the Deployment

In this step, create Config Map configuration for the application *uic* and update the deployment configuration created in Step 1:

1. In the left navigation bar, select **Container > Config Maps**.

2. Click **New Config Map** and provide the following config map information:

   - Application: uic
   - Environment: beta
   - Cluster: beta-k8s-cn4
   - Data: Key - application.properties; Value - the content of the application.properties file
   - Description: Config Map for application *uic* in beta environment 

3. Click the **New Config Map** button to save the config map configuration.

   .. image:: media/config_map_e.png

4. Click **Deployments** in the navigation bar, select the deployment configuration created in Step 1, and then click the **Edit** button.

5. Edit the **Config Map** field in the deployment configuration as shown below:

   .. image:: media/update_config_map_e.png



## Step 3: Configure Service and Route

In this step, create service and route configuration for the application *uic* so that it can expose Web services outside the cluster.

The detailed steps for service configuration are as follows:

1. In the left navigation bar, select **Container > Services**.

2. Click the **New Service** button and provide the following service configuration information:

   - Application: uic
   - Environment: beta
   - Cluster: beta-k8s-cn4
   - Type: ClusterIp
   - Port: 8080, 8080, TCP
   - Description: Service configuration for application *uic* in beta environment 

3. Click the **New Service** button to complete the service configuration.

   .. image:: media/service_e.png

The detailed steps for route configuration are as follows:

1. In the left navigation bar, select **Container > Routes**.

2. Click the **New Route** button and provide the following route configuration information:

   - Application: uic
   - Environment: beta
   - Cluster: beta-k8s-cn4
   - Host: uic
   - Route: /api/user
   - Service: uic-service-dev  
   - Port: 8080
   - Description: Route configuration for application *uic* in beta environment 

3. Click the **New Route** button to complete the route configuration.

   .. image:: media/route_e.png

## Step 4: Create a Pipeline

In this step, create a pipeline for the application *uic*. A pipeline consists of basic information, stages, and jobs. Take the following steps to create a pipeline:

### Configuring Basic Information

1. In the left navigation bar, select **Development > Pipeline**.

2. Click the **New Pipeline** button and provide the following basic information of the pipeline:

   - Application Name: uic
   - Pipeline Name: uic-pipeline-dev
   - Language/Version: java_1.8.0
   - Tool: maven_3.3.9
   - Triggering Mode: Manual

   .. image:: media/pipeline_basic_e.png

### Configuring Stages

1. Select the **BUILD** stage, and provide the following information:

   - Job Name: Build

   - Docker File Path: Dockerfile

   - Docker Registry: harbor.eniot.io

     .. image:: media/task_build.png

1. Select the **SCAN** stage, and provide the following information:

   - Job Name: Sonar Scan

   - Source Code: src/main/java

     .. image:: media/task_code_scan.png

   .. note:: For a detailed description for build and code scan rules, see [Creating Pipelines](../howto/pipeline/creating_pipeline).

4. Select the **DEPLOY** stage, and provide the following information:

   - Environment: beta

   - Job Name: Deployment

   - Cluster: beta-k8s-cn4

   - Resource Type: Deployment

   - Resource Name: uic-deployment-dev

     .. image:: media/task_deployment.png

5. Click the **New Pipeline** button to save the pipeline configuration.

## Step 5: Run the Pipeline and View the Results

Run the configured pipeline and view the pipeline running results.

1. In the list of pipelines, click the created pipeline *uic-pipeline-dev* to open the pipeline details page.

2. Click the **Run** button, select the GitLab branch, and click **Run**.

   .. image:: media/run_pipeline_e.png

3. View the running results of the pipeline.

   - Click on **Build** to view the running results of the build job, including the build log and the image address:

     .. image:: media/build_result.png

   - Click on **Scan** to view the results of the code scanning job, including the scanning log and scanning result address:

     .. image:: media/scan_result.png

   - Click on **Deploy** to view the results of the deployment job:

     .. image:: media/deploy_result.png



## Step 6: Test the Published Application

After the application is deployed successfully, test running the application to ensure that the application service can run normally according to the configured service information.

<!--end-->