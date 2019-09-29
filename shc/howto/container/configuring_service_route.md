# Configuring Services and Routes

This topic describes how application developers can create new service configuration so that applications can expose Web services outside the cluster, as well as how to configure corresponding routes.

## Prerequisites

Before creating a new service, you need to complete the deployment configuration. For detailed steps, see [Configuring Deployments](configuring_deployment).

## Creating Service

You can create a new service for your application as per the following steps:

1. In the left navigation bar, select **Container > Services**.

2. Click the **New Service** button and complete the detailed configuration of the service.

3. Provide the basic information for the service:

   - **Application**: Select the application that needs to publish the service.
   - **Environment**: Select the service environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.
   - **Type**: Select the service type, where only ClusterIP is supported currently.

4. Complete the port configuration for the service by entering the port and target port for the service and selecting the protocol type.

  - **Port**: The port to be used by the internal clients of the cluster to access the service.
  - **Target port**: The port on the pod. The data received from the service port finally flows through the kube-proxy to the target port of the backend pod and then to the container.
  - **Protocol**: Protocol supported by the ports, where you can select TCP or UDP.

  .. image:: ../../media/service_config.png

5. Enter the description for the service.

6. Click the **New Service** button to complete the configuration.

## Creating routes

You can create a new route for your application as per the following steps:

1. In the left navigation bar, select **Container > Routes**.

2. Click the **New Route** button and complete the detailed configuration of the route.

3. Provide the basic information for the route:

   - **Application**: Select an application that requires the route.
   - **Environment**: Select the route environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.

4. Configure the route rules:

   - **Host**: Depends on default cluster settings, and can not be modified.

   - **Route**: Enter the path to access the external service.

   - **Service**: Select the service you have created.

   - **Port**: Select the port, where only 8080 can be selected.

     .. image:: ../../media/route_config.png

5. Enter the description for the route.

6. Click the **New Route** button to complete the configuration.

## Next Step

After the service and route are created, you can clone, edit and delete them as needed. The specific steps are similar to those for [Configuring Deployments](configuring_deployment).

<!--end-->
