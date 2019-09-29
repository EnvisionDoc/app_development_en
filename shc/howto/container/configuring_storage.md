# Configuring Storage

This topic describes how application developers can create new storage configuration to support the data storage needs of applications.

## Creating Storage

Create storage configuration for your application as per the following steps:

1. In the left navigation bar, select **Container > Storage**.

2. Click the **New Storage** button and complete the detailed configuration of the storage.

3. Provide the basic information for the storage:

  .. image:: ../../media/storage_config.png

   - **Application**: Select an application that requires the storage.
   - **Environment**: Select the storage usage environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.
   - **Storage Type**: Select a storage type, supporting Block and Filesystem.
   - **Access Mode**: Select an access mode, supporting ReadWriteOnce (mounted in read/write mode to exactly 1 host) and ReadWriteMany (mounted in read/write mode to many hosts).
   - **Storage**: Enter the storage capacity (GB) that is required by the application.
   - **Description**: Enter the description for the storage.

4. Click the **New Storage** button to complete the configuration.

## Next Step

After the storage configuration is created, you can clone, edit and delete it as needed. The specific steps are similar to those for [Configuring Deployments](configuring_deployment).

<!--end-->
