# Integrating Third-party Plugins

Application Portal supports integration of third-party plugins for use by users within the enterprise  or organization.

## Prerequisites

The system administrator needs to ensure that third-party plugins are legally available and obtain the plugin's URL for registration.

## Register a Plugin

The system administrator can register third-party plugins by taking the following steps:

1. Log in to the Application Portal admin console, click **Plugin Management** from the navigation bar, and then click **Register Plugin**.

2. Enter the name of the plugin in Chinese and Englsih, URL, and description of the plugin.

3. Click **Submit** to complete the plugin registration.

   .. image:: ../media/registering_plugin.png
      :width: 300px

## Assign a Plugin

Once a plugin is registered, you can assign the plugin to the organization that needs to use the plugin:

1. In the list of registered plugins, find out the target plugin and click the **Assign OU** icon.

2. In the OU list, select the organization to assign the plugin to.

3. Click Submit to complete the plugin assignment.

   .. image:: ../media/assigning_plugin.png

The OU administrator can then use the assigned plugin under the **Plugin Management** menu of the admin console.

## Manage a Plugin

The system administrator can perform the following management operations on registered plugins:

1. Click the **Assign OU** icon to assign a plugin to more organizations or remove an organization to which the plugin has been assigned.
2. Click the **Edit** icon to update the plugin name, URL, or description.
3. Click the **Delete** icon to remove the registered plugin. Before removing a plugin, you must ensure that the plugin is no longer needed for all organizations to which the plugin has been assigned.

<!-- end -->
