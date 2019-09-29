# Configuring Database Service

EnOS SHC provides Redis, MySQL and Mongo database services for application deployment and publish. You can configure the appropriate database for your applications based on your business needs.

## Creating Database Configuration

Taking Redis for example, you can create a database configuration by taking the following steps:

1. In the left navigation bar, select **Service Catalog > Redis**.

2. Click the **New Redis** button to complete the database service configuration:

   - **Instance Name**: Enter the Redis instance name, where the default prefix is *redis-{project-name}-*.
   - **Environment**: Select the Redis usage environment, where you can select alpha, beta, prod, dev, or ppe.
   - **Cluster**: Select the cluster location for Redis.
   - **Storage**: Select the storage capacity of the created Redis database, where you can select 1G, 2G, or 4G.
   - **Maximum Memory**: Select the maximum memory available for the Redis database, where you can select 200M, 500M, 1G, or 2G.
   - **Version**: Select the Redis version, where you can select *release 3.2*.
   - **Type**: Select the Redis type, where you can select the *Sentinel* type.
   - **Port**: 6379 by default, and unchangeable.
   - **Password**: Enter your password to access Redis.
   - **Package**: Select a resource package with pre-defined CPU and memory capacity.

3. Click the **New Redis** button to save the configuration.

   .. image:: ../media/redis_config.png

## Next Step

The configuration of MySQL and Mongo database services is similar to that of Redis. You can create other database configuration by following the same steps.

<!--end-->
