---
title: "User Roles"
parent: "project-security"
menu_order: 10
tags: ["studio pro", "user role", "project security", "security"]
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details.
---

## 1 Introduction

A user role aggregates a number of access rights on data, forms, and microflows. An end-user of the application is assigned one or more user roles by an administrator, and gets all access rights that these user roles represent.

Every user role has one or more [module roles](module-security#module-role), which means that users with that user role have all the access rights that are defined for those module roles. A typical user role has module role System.User and at least one other module role.

The purpose of the distinction between user roles and module roles is to make a module self-contained (independent from the project in which it is defined or used), so that it can be reused in different projects and/or published to the App Store.

End-users of your application only see the user roles and not the module roles.

To access user roles, open **Project Security** > **User roles** tab:

![](attachments/user-roles/user-roles-example.png)

## 2 User Role Properties

Double-click the user role to open its properties. 

The user role has the following properties:

*  [**General** properties](#general)

*  [**User management** properties](#user-management)

    ![](attachments/user-roles/user-role-properties.png)

### 2.1 General Properties {#general}

General properties of user roles are described in the table below:

| Property       | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| Name           | The name property defines the name of the user role. This name is shown to end-users who can create or edit user accounts in the application. |
| Documentation  | In this property you can document additional information about the user role. This information is shown to end-users who can create or edit user accounts in the application. |
| Module roles   | A list of module roles of which the access rights are accumulated in the user role. An end-user that is assigned a user role gets all access rights of the module roles of that user role. |
| Check security | This specifies whether the consistency of security settings is checked for this user role. You can choose to not check security for a user role. For example, user roles that are used only for web service users do not need to be checked because they never sign in to the client. See [Project Security](project-security) for more information on the security check. |

### 2.2 User Management Properties {#user-management}

A user role can be allowed to manage users with a number of other user roles (including itself), called manageable roles. This means that end-users who have this user role, can create, view, edit and delete users with at most the manageable user roles.

| Value | Description |
| --- | --- |
| All | End-users with this user role can manage all users and grant all user roles. Usually this option should only be configured for an administrator. |
| Selected | End-users with this user role can manage users that have at most the selected user roles, and can grant only the selected user roles. If no user roles are selected, end-users with this user role cannot manage users at all. |

## 3 Read More

* [Project Security](project-security)
* [Administrator](administrator)
* [Demo Users](demo-users)
* [Anonymous Users](anonymous-users)
* [Password Policy](password-policy)