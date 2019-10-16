# Managing Assets

Application Portal supports for synchronizing the data asset information with EnOS and assigning asset access permissions to created users and user groups. After that, users can view asset information and data through applications.

Asset permission management includes:
- Asset Synchronization: Synchronizing and updating the asset data to Application Portal
- Assigning asset access permissions to users or user groups

## Asset Synchronization

Asset synchronization refers to the synchronization of assets that have been connected to EnOS and identified with the tag `auth_unit:true`, from EnOS to the Application Portal. The asset access permission can be assigned to users only after the synchronization is completed.

1. Log in to the Application Portal admin console and select **Asset Synchronization** from the navigation bar.

2. Click **Synchronize Asset** to start synchronizing new and updated asset data from EnOS to the Application Portal.

  .. image:: ../media/asset_1.png

## Assign Asset Permission

Assign manageable assets to users or user groups. Once such assignment is completed, users can see related asset information and data through applications.

1. Log in to the Application Portal admin console and select **Asset Permission** from the navigation bar.

2. Select a user or user group to view the assets that have been assigned to the user or user group. Click **Manage Asset** to add or remove assets to be assigned to the user or user group.

  .. image:: ../media/asset_3.png

3. The assets assigned can be removed from the user or user group by clicking the **Delete** icon.

  .. image:: ../media/asset_2.png

<!-- end -->
