# Managing Organization Structure

The organization structure is a hierarchical relationship for asset management with nodes as the management unit. After the personnels of an enterprise or organization are assigned to the organization structure, they can use the applications in the specified organizations and access the information and data of specified assets. The OU administrator can perform the following management operations on the organization structure:

- Create/delete an organization structure
- Enable/disable the automatic assignment of organization structure. After the automatic permission assignment is enabled, the users in the organization structure will automatically obtain the access permissions of the subordinate nodes.
- Add child nodes to a node
- View the user information under a node
- Manage the assets under the leaf node, synchronize the assets that are connected and tagged in the organization from EnOS to the Application Portal, and assign asset permissions to organizational nodes after such synchronization is completed.
- Delete/rename a node

## Prerequisites

The OU administrator needs to plan the organization structure to be created according to the actual business needs, for example, by using organization structure or geographic location of the enterprise as the hierarchy.

## Create Organization Structure

1. Log in to the Application Portal, enter the Admin Console, and select **Organization Structure** from the navigation bar.

  .. image:: ../media/ou_structure_1.png

2. Click **New Organization Structure**, enter the name of the organization structure, and click **Submit**.

  .. image:: ../media/ou_structure_2.png

3. After the automatic permission assignment of the organization structure is enabled, users in the organization structure will automatically obtain access permissions of the subordinate nodes. When it is disabled, the system will no longer automatically assign the asset access permissions to users based on the node structure.

## Manage Organization Structure

Click the **Manage** icon for the organization structure to enter the **Manage organization structure** module. You can view the users and assets under the organization structure, add child nodes to the organization structure, assign assets, and rename or delete the organization structure.

.. image:: ../media/ou_struct_overview.png

1. View users and assets: Click on the organization structure to view the list of users and assets that belong to that node on the right side of the page.

2. Add a child node: Click **Add Child Node** and type the node name.

   .. image:: ../media/ou_structure_4.png

3. Manage assets: Click **Manage Asset** to assign the assets synchronized but not assigned to an organizational node, or reset an assigned asset as unassigned. Assets can be assigned and manged only for leaf nodes.

   .. image:: ../media/ou_structure_6.png

   For more information about asset synchronization, see [Managing Assets](managing_asset_permission).

4. Rename: Click **Rename** to rename an organizational node.

   .. image:: ../media/ou_structure_9.png

5. Delete an organization structure: Click **Delete**, or click the **Delete** icon on the **Organization Structure** page to delete an organization structure. Remember that this operation is irrevocable. Any organization structure for which users or assets have been assigned cannot be deleted.

   .. image:: ../media/ou_structure_7.png

## Next Step

After an organization structure is created, you need to assign new assets to the organizational nodes through the assets management function under the leaf nodes if any new assets are synchronized to the Application Portal, and the information and data of the new assets are accessible only for the users in the organizational nodes.

After you create a new user for your organization, you need to assign the user to the created organization structure. After a user logs in to the Application Portal, you can choose to assign an organization structure to the user. For details about how to manage users, see [Managing Users](managing_users).

<!-- end -->
