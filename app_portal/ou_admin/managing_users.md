# Managing Users

The OU administrator can perform the following management operations for users in the organization:

- Adding a user: add a user who has an account created in the system to the current enterprise or organization; create an account for a user who has no account created, and add the user to the enterprise or organization
- Importing users in batch: import users in batch by an Excel file
- Removing a user: remove an existing user from your enterprise or organization
- Assigning a role to a user; removing a user's role
- Assigning an organization structure to a user; removing a user from an organization structure
- Adding a user to a user group; removing a user from a user group

## Prerequisites

The OU administrator has created organization structures, roles and user groups in the admin console.

## Add a User

You can add a user to your enterprise or organization by taking the following steps:

1. Go to the admin console, and select **User** from the left menu bar to open the list of users.

2. Click the **Add User** button and type the user's email address for search purpose. If an account corresponding to this email address already exists in the system, you can directly select the user and add the user to the enterprise or organization.

   .. image:: ../media/user_1.png
      :width: 300px

3. If the user account does not exist, you can click **Create a user account** to create an account.

   .. image:: ../media/user_2.png
      :width: 300px

4. Edit the account name (mailbox prefix by default) and click **Submit**. Once submitted, the account cannot be modified.

   .. image:: ../media/user_3.png
      :width: 300px

After the creation is completed, the user will receive a notification email containing a link to set the account password.

### Import Users

You can import users in batch to your enterprise or organization by taking the following steps:

1. On the User List page, click the **Batch Import** button.

2. Click **Download templates** to download the template and edit the information of users to be imported in batch by following the instructions in the template file.

3. Upload the well-edited template file and view the user importing results. If such import fails, click **Download failed records**, modify the file, and then upload it again.

   .. image:: ../media/importing_user.png

### Remove a User

You can remove existing users out of your enterprise or organization by taking the following steps:

1. In the list of users, find out the user to be removed.

2. Click **Remove from Enterprise/Organization** icon on the right side of the user list, and click **Confirm**.

   .. image:: ../media/user_4.png
      :width: 300px

After confirming the removal, the user will not be part of the enterprise or organization.

## Assign a Role to a User

You can assign roles to existing users by taking the following steps:

1. In the user list, find out the user to be managed and click the **Manage** icon on the right of the user list.

2. On the **User Details** page, click the **Edit** button to edit the user's name and phone number; click the **Reset Password** button and confirm, and the system will send an email for password resetting to the user.

   .. image:: ../media/user_5.png
      :width: 300px

3. Click the **Assign Role** button to select the role to be assigned to the user (multiple choices are allowed). Once a role is assigned to a user, the permissions corresponding to that role will be granted to the user.

   .. image:: ../media/user_6.png

### Remove a User's Role

You can take the following steps to remove a user's role:

1. In the list of assigned roles, find out the role to be removed.

2. Click the **Remove Role** icon and confirm.

   .. image:: ../media/user_7.png
      :width: 300px

After a role is removed, the user will no longer have the permissions granted for that role. That role can be reassigned to the user if needed.

## Assign Organization Structure to a User

You can assign organization structures to existing users by taking the following steps:

1. On the **User Details** page, click the **Assign Organization Structure** button.

2. In the pop-up window, select the organization structure to be assigned to the user (where multiple choices are allowed, and if you select a parent node, any subordinate node under it cannot be checked, but the permissions of the subordinate node are granted by default), and then click **Confirm**.

   .. image:: ../media/user_8.png

After a user joins an organization structure, the corresponding permissions to view assets in the organization structure are granted to the user.

### Remove a Users from Organization Structures

You can remove users from your organization structure by taking the following steps:

1. In the list of assigned organization structures, find out the target organization structure.

2. Click **Remove from Enterprise/Organization** icon and confirm.

   .. image:: ../media/user_9.png
      :width: 300px

Once being removed from the enterprise or organization, users will no longer have the permissions related to the organization structure. That organization structure can be reassigned to the user if needed.

## Add a User to a User Group

You can add an existing user to a user group by taking the following steps:

1. On the **User Details** page, click the **Assign User Group** button.

2. In the pop-up window, select the user group to be assigned to the user (where multiple choices are allowed), and then click **Confirm**.

   .. image:: ../media/user_10.png

After a user joins a user group, the corresponding permissions to view assets in the user group are also granted.

### Remove a User from a User Group

You can take the following steps to remove a user from a user group:

1. In the list of assigned user groups, find out the user group to be removed.

2. Click **Remove from User Group** icon and confirm.

   .. image:: ../media/user_11.png
      :width: 300px

Once being removed, the user will no longer have the permissions granted for that user group. The user can be added to the user group if needed.
