# Basic Operations in Application Portal

EnOS Application Portal provides users with a unified portal to access applications of multiple domains, enabling easy and quick access of applications across enterprises and organizations.

The main functions of the application portal include:
- List of applications by categories
- Switching among enterprises or organizations
- Centralized message center for all applications
- Switching language
- User information and password
- Help center for applications
- Entry to the Admin Console (for administrators only)

## Basic Operations

1. Enter the Application Portal login page URL in the browser, in the format of `https://app-portal.{domain_name}/login`.

   .. note:: The `domain_name` in the URL is the domain name for deploying the Application Portal service. Different cloud services and instances have different service addresses, please contact the Envision project manager or technical support for corresponding service information.

2. Enter your account and password to log in. If you forgot your password, you can click **Forgot Password** to reset the password. After logging in, select the enterprise or organization you want to enter. If there is only one enterprise or organization, you will enter the organization directly.

   .. image:: ../media/portal_login.png

3. After logging in successfully, you will enter the homepage of the first application in the application list by default. If you do not have permissions to access any application, the page will report an error. In that case, you can contact the OU administrator to obtain appropriate application permissions.

   .. image:: ../media/portal_home_page.png

4. Switching among applications: Click the application list in the top left corner of the page to view the list of all applications that are enabled and accessible. Click the application name to switch to the application you want to use.

   .. image:: ../media/portal_app_list.png

   .. note:: If you do not have the permissions to access the application you want to access or any menu in it, the page will report an error. In that case, you can contact the OU administrator to obtain appropriate permissions for the application or its menus.

5. Switching among languages: Click the User Information drop-down list in the upper right corner of the page, select **Switch Language** to switch between Chinese and English.

   .. image:: ../media/portal_switch_lang.png

6. Changing the password: Click the User Information drop-down list in the upper right corner of the page and select **Change Password** to reset the password.

7. Switching among enterprises or organizations: Click the User Information drop-down list in the top right corner of the page, select **Change Enterprise / Organization**, and then select the enterprise or organization you want to enter.

8. Message Center: Click the bell icon in the upper right corner of the page to view the real-time alert information pushed by applications.

   .. image:: ../media/portal_message_center.png
      :width: 300px

   For more information about the Message Center, see [Managing Application Messages](managing_messages).

9. Help Center: You can go to the Help Center of applications by clicking the question mark icon in the upper right corner of the page.
