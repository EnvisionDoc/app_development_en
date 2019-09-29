# Configuring Alarm Service

EnOS SHC alarm service supports setting customized alert rules. With these rules, an alert will be sent to notify relevant personnel when the number of events generated from the application deployment and pubish process reaches the set threshold.

## Configuring Alert Rules

You can follow the steps below to configure the alarm rules for your applications:

1. In the left navigation bar, select **Alerts**.

2. Click the **New Alert Rule** button to complete the alert rule configuration:

   - **Rule Name**: Enter the name of alert rule.

   - **Application Name**: Select the application name to be configured with the alert service.

   - **Application Log Configuration**: Select the configured application log service.

   - **Rule Type**: Select the alert rule type, where only FREQUENCY is supported for now. If the number of logs that meet the filtering criteria exceeds the set threshold within the specified time range, the alert will be triggered.

   - **filter**: Enter the filter criteria (e.g. code:200) to filter out eligible logs.

   - **timestampField**: Enter a timestamp, which will be used to filter data by time. If not specified, you can not narrow the data range by time range.

   - **eventCount**: Enter the threshold for the number of events. When the number of logs generated within a certain time range exceeds this threshold, an alert will be triggered.

   - **timeFrame**: Enter the alert time window, and compare the number of logs in the statistics window with the threshold.

     .. image:: ../media/alert_rule.png

3. Click the **New Alarm Rule** button to save the configuration.

<!--end-->
