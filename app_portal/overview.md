# About Application Portal

EnOS Application Portal is a universal and flexible portal for permission management and unified login for application access. It provides application developers with a unified RBAC-based permission system and login portal, and helps to ensure that end users can smoothly access and use applications in a same system under a same set of users and permissions and same experience, improving security control and reducing R&D costs.

Application Portal is an unified EnOS-based application login portal. Its system architecture is as follows:

.. image:: media/architecture.png

## Main Functions

The main functions of EnOS Application Portal include:

- RBAC-based permission management, including role, permission, user group, organization structure, and other general capabilities
- Automatic authorization of assets through asset management hierarchy
- Hierarchical authorization management through sub administrator configuration
- Application menu configuration for user's cross-application access
- Unified portal and personalized configuration for multiple OU access
- Real-name certification, multi-factor authentication, and security level protection (in planning)

The above-mentioned functions work on the basis of the interaction of Application Portal with the applications, assets, permissions and other modules of EnOS. The Application Portal consists of two major modules: application portal and admin console. This documentation introduces, from the perspectives of application developer, system administrator, OU administrator, and application user, the interaction between Application Portal and EnOS as well as the the functions and usage of the two modules.

## Related Roles

EnOS Application Portal serves mainly for the following roles:

**Application developer**

Develop applications offline based on the API and SDK provided by EnOS. An application developer can be the inhouse developer of an enterprise or organization, or a third-party application developer. The application developer needs to configure the applications appropriately so that they can be synchronized to and displayed in the Application Portal.

**System administrator**

Initialize the Application Portal, create and assign the OU administrator, and register plug-in applications for an enterprise or organization.

**OU administrator**

The IT or system operation and maintenance personnel in an enterprise or organization. The OU administrator can log in to the Application Portal and enter the admin console with the account assigned by the system administrator, and is responsible for the overall management of the classification, users and permissions, and assets for the applications of an enterprise or organization.

**Application user**

The actual user of an application. A user can log in to the Application Portal with the account created by the OU administrator, and can use the applications developed or purchased by an enterprise or organization to view or manage the assets that are authorized to access, and perform appropriate authorized operations.

## Related Services

### Device Management

The EnOS Device Management Service helps you quickly connect physical devices securely to the EnOS cloud for data transfers, manage device cycles, and map the asset structure in the physical world to the digital world. [Learn more >>](/docs/device-connection/en/latest/device_management_overview.html)

### Data Asset Management

The EnOS Data Asset Management Service provides stream data processing, time series data management, data quality, data subscription and other services. [Learn more >>](/docs/data-asset/en/latest/data_asset_overview)

### Application Enablement

You can develop applications by using the EnOS SDK and access EnOS services and resources through the EnOS APIs. [Learn more >>](/docs/app-development/en/latest/app_dev_overview.html)
