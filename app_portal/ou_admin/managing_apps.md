# Managing Applications

The applications registered or purchased through the EnOS Console can be automatically synchronized to the Application Management page in the admin console of Application Portal. The OU administrator can perform the following management operations for the applications in the organization:

- Enable or disable applications registered or purchased by the OU
- Assign organization structures to applications
- Set the menu group of an application
- Sort applications
- Create an application shortcut

## Prerequisites

1. The application developers of an enterprise or organization need to register the applications in the EnOS Console and create the application menus and permissions.

2. Enterprise or organization can purchase third-party applications through EnOS Console. The OU administrator needs to submit the purchasing request on the Application Registration page of EnOS console. After receiving the purchase request, the third-party application developer approves the purchasing request from the OU and authorizes the enterprise or organization with the menus and permissions for accessing the application.

For more information about how to manage applications through the EnOS Console, see [Managing Applications](../../app_management/managing_apps).

## Enable and Disable Applications

The applications registered and purchased through the EnOS Console can be automatically synchronized to the Application Management page in the Application Portal. The OU administrator can enable and disable the application by taking the following steps:

1. Go to the admin console, select **Application Management** from the left menu bar and open the list of applications.

2. In the **Enable** column of the application list, you can enable/disable an application by toggling the switch.

   .. image:: ../media/enable_apps.png

After an application is enabled, users in the OU who have permissions to the application will be able to see the application. After an application is disabled, all users in the OU cannot see the application in the application list, but the usage permissions for the application configuration remain unchanged.

## Assign Organization Structure to an Application

Once an organization structure is assigned to an application, all users within the organization structure can use the application. You can assign organization structures to an application by taking the following steps:

1. Find out the target application in the application list and click the **Assign Organization Structure** icon.

2. In the pop-up window, select the created organization structure to assign to the application, and click **Confirm**.

   .. image:: ../media/apps_2.png

## Manage Menu Groups

By managing menu groups, you can configure the menu structure and combinations that need to be displayed within an application. You can manage the menu groups by taking the following steps:

1. Find out the target application in the application list and click the **Manage Menu Group** icon.

2. In the **Menu Group** column, click + to create a menu group.

   .. image:: ../media/apps_5.png

3. For existing menu groups in the application, you can select **Rename/Delete** to rename or delete them.

   .. image:: ../media/apps_3.png

4. Select a menu group, and click the **Configure Menu** button to configure the in-application menu items for the menu group, where it is allowed to select multiple items (once an upper menu is checked, all the subordinate menus under it will be checked by default).

   .. image:: ../media/apps_4.png

## Sort Applications

With the application sorting function, you can adjust the order by which all the applications and application shortcuts in your application list appear.

1. On the Application List page, click the **Sort Applications** button.

2. In the pop-up window, drag the application names to sort the applications, and then click **OK**. The application list will display the applications in the new order.

   .. image:: ../media/ordering_apps.png

## Create an Application Shortcut

The Application Portal supports creation of application shortcuts, which can integrate the modules or menus of different applications to form a new application. For more information about application shortcuts, see [Creating Application Shortcuts](creating_app_shortcut).

<!-- end -->
