# Managing Applications

This topic describes how project administrator can create an application and manage application members and other basic information of the application.

## Creating an Application <newapp>

The project administrator for application development and deployment can create an application by taking the following steps:

1. Open the project overview page by clicking the project name in the project list.

2. In the left navigation bar, select **Application**, then click **New Application**.

3. Enter the application name and select the application development language.

4. Enter the application GitLab repository. The repository can be left blank here, and be edited in application **Basic Information** after it is generated.

5. Enter a description for the application and click **Next Step**.

   .. image:: ../../media/create_app.png

6. Select one or more application members and the member role, click **Add Member**, then click **Next Step**.

   .. image:: ../../media/add_member.png

7. Configure detailed container deployment information for the application. Click **Skip** to skip the configuration if you want to configure the container information after the application is created. Application developers can complete the configurations later. For details, see [Managing Container Configurations](../container/index.html).

Once the application is created, you can view its basic information by clicking on the application name in the application list.

## Editing Application Information

The project administrator or application owner can edit the basic information of any created applications.

1. In the left navigation bar, select **Application**. In the application list, click the application name to open the application details page.

2. In the **Basic Information** section, click **Edit** to update the development language and description of the application. Click **Delete** and confirm to delete the application.

3. For **Git Repository**, click **Edit** to update the application's code repository.

   .. image:: ../../media/app_overview.png

4. In the **Application Pipeline Overview**, view the running history of the application, including the pipeline name, the number of successful and failed jobs, and more.

   .. image:: ../../media/app_pipeline_overview.png

5. Under the **Member** tab, you can add application members, search memeber, update existing member information, or remove members.

   .. image:: ../../media/app_member.png

6. Under the **Deployment** tab, you can view the deployment information of the application, or edit the container configuration.

   .. image:: ../../media/app_deploy.png


<!--end-->
