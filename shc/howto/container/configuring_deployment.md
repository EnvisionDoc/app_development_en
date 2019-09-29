# Configuring Deployments

This topic describes how application developers can configure deployment information for applications to be published.

## Prerequisites

Before creating a new deployment, you need to complete the application creation and the basic information configuration of the application. For detailed steps, see [Creating Applications](../admin/managing_app#newapp).

## Creating Deployment

The deployment information of the application can be configured by two modes: **Config** and **Yaml**. Taking the **Config** mode as an example, create a new deployment for the application by the following steps:

1. In the project list, click on the project name to enter the project space.

2. In the left navigation bar, select **Container > Deployments**.

3. Click the **New Deployment** button and complete the detailed configuration of the deployment.

4. Provide basic information about the deployment:

   - **Application Name**: Select the application to be deployed.
   - **Environment**: Select the application deployment environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.
   - **Replicas**: Enter the number of replicas required.

5. Configure the computing **Resource Quota** required to run the application, including CPU and memory quota. As show below:

   .. image:: ../../media/deployment_config.png

6. (Optional) Set the **Environment Variable** and value for running the application.

7. (Optional) Select the **Config Map** configuration that needs to be injected into the container and enter the mount path. For details on configuring the Config Map, see [Configuring Config Maps](configuring_configmap_secret).

8. (Optional) Set the **Log Path** for storing the log files.

9. (Optional) Select the **Storages** configuration for the application and enter the mount path. For details on configuring the storage, see [Configuring Storage](configuring_storage).

10. (Recommended) Configure **Readiness Probe** for the container to check if the container is ready. The configuration information of the readiness probe includes the detection task timeout time (seconds), the detection period (seconds), the number of retry times, the detection initial delay (seconds), and the handler and parameters of the probe. For details about container probes, see [Pod Lifecycle](https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#container-probes).

  .. image:: ../../media/probe.png

11. (Optional) Configure the **Liveness Probe** for the container with its configuration information similar to the Readiness Probe.

12. Set **Minimum Readiness Time** of the container (seconds).

13. Enter the description for the deployment.

14. Click the **New Deployment** button to complete the configuration.

## Managing Deployment

After the application deployment configuration is created, you can clone, publish, rollback, scale, edit, or delete the deployment by clicking "...".

.. image:: ../../media/edit_deployment.png

- **Clone**: Click **Clone** of an existing deployment to reuse the deployment configuration information and quickly create a new deployment.

- **Publish**: Click **Publish** of a deployment, and configure the information required:

   - In the **Publish Operation** section, select a docker image, and click the **Start** button.

     .. image:: ../../media/publish_deployment.png

   - View the publishing results and history of the deployment.

     .. image:: ../../media/publish_result.png

- **History Records**: Click **History Records** of a deployment to view all the history operations to the deployment. Click **Details** to view the history configuration of the deployment; click **Rollback** to roll the current deployment back to the selected configuration.

   .. image:: ../../media/rollback_deployment.png

- **View Details**: Click **View Details** to view the detailed configuration of the deployment.

- **Autoscaler**：Click **Autoscaler** of a deployment to change the configuration of replicas, average CPU utilization, and average memory.


- **Edit**: Click |edit| of a deployment to update the deployment configuration information.

  .. |edit| image:: ../../media/icon_edit.png

- **Delete**: Click |delete| of a deployment and confirm, then you can delete the deployment configuration information.

  .. |delete| image:: ../../media/icon_delete.png


<!--end-->
