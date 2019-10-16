# Terminology

This article describes the terminology involved in Application Portal.

## Organization structure

The organization structure is a hierarchical relationship for asset management with nodes as the management units (for example, setting the hierarchy by geographic location). After the personnels of an enterprise or organization are assigned into the organizational structure, they can use the applications in the specified organizations and access the information and data of specified assets. It is helpful for enterprises or organizations to achieve centralized and hierarchical management of users, applications, and asset data.

## Application

The applications registered or purchased through the EnOS console can be automatically synchronized to the Application Portal. An OU administrator can enable or disable an application, assign an application to an organization node within an organization structure, manage menu groups of applications, or combine menus of multiple applications into a new application based on the business needs of the enterprise or organization.

## Menu group

A menu group is a collection of menus displayed in an application, which is formed by combining the created menus. Once a menu group is assigned to a role, the role has the permissions to access any menus in the menu group. The application's menus are configured by the application developer via the application registration page in the EnOS console.

## Permission

Permission is the privilege name that is named in an application and has specific operations. When permission is assigned to a role, the user of that role would have the appropriate operational capabilities within the application. The application's permission is configured by the application developer via the application registration page in the EnOS console.

## Role

A role is a collection of functional permissions, including menu access permissions and operational permissions. After assigning a role to a user, the user of that role would gain access to the corresponding menus and operation permissions within the application.

## User group

A user group is formed by grouping the users within an organization, and users in the same user group have the same asset access permissions. You can assign asset permissions through user groups to improve management efficiency.

## Asset permission

The organization assets registered in the EnOS console can be synchronized to the Application Portal by the asset synchronization function. The OU administrator assigns assets to the organization nodes and assigns asset permissions to users or user groups within the organization. Users with appropriate permissions within the organization can view asset information and data through applications.

## Sub administrator

Sub administrators can manage the appropriate personnel permissions, such as assigning roles and assigning asset access permissions, within a specific organization structure. An OU administrator can add a user within an organization as sub administrator and specify organization nodes and roles that the sub administrator can manage.
