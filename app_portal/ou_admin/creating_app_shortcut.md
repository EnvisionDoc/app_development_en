# Creating Application Shortcuts

Application Portal supports the creation of application shortcuts, which can integrate the modules or menus of different applications to form a new application to meet the needs of different business scenarios.

## Prerequisites

The enterprise or organization has registered or purchased applications for creating shortcuts, and the organization has obtained the permissions to configure menus from multiple applications.

## Create an Application Shortcut

The OU administrator can create a shortcut of an application by taking the following steps:

1. Log in to the Application Portal admin console and select **Application Management** from the navigation bar.

2. In the list of applications, find out the application for which a shortcut needs to be created, move the cursor over the **More** icon, and select **New Shortcut**.

   .. image:: ../media/create_shortcut.png

3. On the **Shortcut Details** page, click **Edit** to edit the name, category, and description of the application shortcut.

   .. image:: ../media/update_shortcut.png

4. Go back to the application list page, and in the **Application Name** column, you can view the application shortcut you created. A **Shortcut** icon is displayed next to the name of the application shortcut, which is different from the main application.

   .. image:: ../media/created_shortcut.png

## Combine Application Menus

Once an application shortcut is created, the application shortcut will inherit all valid menus and menu structure of the main application by default. You can combine new menus for the application shortcut by adding or subtracting menus.

1. In the list of applications, find out the application shortcut just created, move the cursor over the **More** icon, and select **Manage Shortcut**.

2. Go to the **Shortcut Details** page, and in the **Added Menus** column, move the cursor to view the main application from which the menu inherits. You can click the **Delete** icon to remove any menu.

   .. image:: ../media/delete_menu.png

3. (Optional) From the **Add Menu** drop-down menu, select **New First-class Menus** to create a new level 1 menu for the application shortcut.

4. (Optional) From the **Add Menu** drop-down menu, select **Add from Other Applications** to get more menus from other applications to which your organization has permissions. Then combine the menus from multiple applications into the created application shortcut.

   .. image:: ../media/menu\_from\_another_app.png

## Manage Application Shortcuts

The management operations for the created application shortcuts are basically the same as for the main applications, including enabling, disabling, assigning organization structures, and managing menu groups.

If the atomic menu in the application shortcut is de-authorized, the menu will be automatically deleted; if the main application is de-authorized, the application shortcut will be automatically deleted.

To delete an application shortcut, move the cursor over the **More** icon and select **Delete Shortcut**.

<!-- end -->
