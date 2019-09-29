# Deploying and Previewing Graph

After completing the configuration of the graph page, you can export the graph as an .SVG file and deploy it on the Web server.

## Prerequisites

Before deploying the graph to the Web server, ensure that the service account (SA) of the application built with EnOS Graph Editor has been authorized to access asset data. Otherwise, the bound dynamic data cannot be displayed on the preview page. For more information about authorizing the SA account, see [Managing Service Accounts](/docs/iam/en/2.0.9/howto/service_account/managing_service_account.html).

## Procedure

1. Select **File > Export SVG ...** from the menu.

2. Export the graph as an .SVG file and save it in local directory.

3. Select **File > Upload SVG** from the menu.

4. In the **Upload File** window, select the directory to save the deployed file. If an asset tree or asset has the `type=HMI` tag, the graph file cannot stored under the asset name directory. This asset can be considered as a "site" or "plant".

5. Select the language of the deployment environment.

6. Click **Add Files**, browse and select the .SVG file to be uploaded, and click **Upload**.

   .. image:: media/uploading_svg.png
      :width: 500px

7. The uploaded .SVG file will be displayed in the **Files** section. Right-click the uploaded .SVG file, and select **Preview**.

   .. image:: media/preview.png
      :width: 200px

8. In the browser window, enter your EnOS account and password to log in the web page to preview the deployed data monitoring page.

   .. image:: media/preview_login.png
      :width: 400px

9. Check the layout of the deployed page and displayed asset data.

   .. image:: media/preview_data.png
      :width: 400px

   .. note: The preview page only displays data of the assets that the logged in account has access to.

10. If you need to further edit the page, update the graph file, export it as an .SVG file, and deploy it to the Web server again.
