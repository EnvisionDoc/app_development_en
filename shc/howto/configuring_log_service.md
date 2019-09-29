# Configuring Log Service

EnOS SHC log service aggregates logs about application development and publish for unified management, helping application development and operation teams to quickly troubleshoot problems.

## Configuring Log Service for Cluster

You can configure log service for the cluster by taking the following steps:

1. In the left navigation bar, select **Logs > Cluster Configuration**.

2. Click the **New Cluster Config** button to complete the cluster log service configuration:

   - **Cluster Name**: Enter the cluster name to be configured with the log service.

   - **Type**: ES.CONTAINER.LOG by default.

   - **hostname**: Enter the host name.

   - **port**: Enter the port number.

   - **scheme**: Select scheme for the log service.

     .. image:: ../media/cluster_log.png

3. Click the **New Cluster Config** button to save the configuration.


## Configuring Log Service for Applications

You can configure log service for your applications by taking the following steps:

1. In the left navigation bar, select **Logs > Application Configuration**.

2. Click the **New Application Config** button to complete the application log service configuration:

   - **Application Config Name**: Enter the name of the log service configuration.

   - **Application Name**: Select the application name to be configured with the log service.

   - **Cluster**: Select the configured cluster log service.

   - **Indices format**: Enter the indices format of the application search log.

   - **Timestamp Field**: Enter a timestamp, which will be used to filter data by time.

     .. image:: ../media/app_log.png

3. Click the **New Application Config** button to save the configuration.

## Querying Logs

You can take the following steps to query the application deployment and publish related logs:

1. In the left navigation bar, select **Logs > Log**.
2. Select the name of the application to be queried as well as the start and end time for log query.
3. Enter the filter criteria and click the **Search** button. The log information that matches the query criteria are displayed on the page.
4. Click **View Context** of each log to view the selected log and other sequential logs before and after the selected one.



<!--end-->