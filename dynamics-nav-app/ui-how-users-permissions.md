---
title: Assign User Permissions and Create or Modify Permission Sets
description: Describes how add Microsoft 365 users to Dynamics NAV, and then assign permissions, access rights, and security settings.
author: edupont04

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 07/12/2018
ms.author: edupont

---
# How to: Manage Users and Permissions
If you get a new employee, your company's system administrator or IT pro has to add them to your [!INCLUDE[d365fin](includes/d365fin_md.md)]. Then, you can assign them access to the relevant parts of the product based on their work area by assigning user groups and permissions.

Permission sets define which database objects, and thereby which UI elements, users have access to, and in which companies.

A permission set is a collection of permissions for specific objects in the database. All users must be assigned one or more permission sets before they can access [!INCLUDE[d365fin](includes/d365fin_md.md)]. A number of predefined permission sets are provided by default. You can use these permission sets as already defined, modify the default permission sets, or create additional permission sets.

You can add users to user groups. This makes it easier to assign the same permission sets to multiple users.

Administrators can use the **User Setup** window to define periods of time during which specified users are able to post, and also specify if the system logs the amount of time users are logged on.

## To assign permissions to a user
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Users**, and then choose the related link.
2. Select the user that you want to assign permission to.
Any permission sets that are already assigned to the user are displayed in the **Permission Sets** FactBox.
3. Choose the **Edit** action to open the **User Card** window.
4. On the **User Permission Sets** FastTab, on a new line, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## To group users in user groups
You can set up users groups to help you manage permission sets for groups of users in your company. You can use a function to copy all permission sets from an existing user group to your new user group. User group members are not copied.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Groups**, and then choose the related link.
2. Alternatively, in the **Users** window, choose the **User Groups** action.
3. In the **User Groups** window, select an existing user group that you want to copy, and then choose the **Copy User Group** action.
4. In the **New User Group Code** field, specify the name of the new user group, and then choose the **OK** button.

    As an alternative to copying, you can choose the New action to create a new line for an empty user group, which you then fill in manually.
5. To add new or additional users, in the **User Group** window, choose the **User Group Members** action.
6. In the **User Group Members** window, on a new line, fill in the fields as necessary by selecting from existing users.
7. To add new or additional permission sets, in the **User Group** window, choose the **User Group Permission Sets** action.
8. In the **User Group Permission Sets** window, on a new line, fill in the fields as necessary by selecting from existing permission sets.

## To create or modify permission sets
If the default permission sets that are provided with [!INCLUDE[d365fin](includes/d365fin_md.md)] are not sufficient or not appropriate for your organization, you can create new permission sets. And if the individual object permissions that define a permission set are not adequate, you can modify a permission set. You can create a permission set manually, or you can use a recording function that records your actions as you navigate through a scenario and then generates the required permission set.

### To create or modify permission sets manually
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Users**, and then choose the related link.
2. In the **Users** window, choose the **Permission Sets** action.
3. In the **Permission Sets** window, choose the **New** Action.
4. On a new line, fill in the fields as necessary.
5. Choose the **Permissions** action.
6. In the **Permissions** window, fill in the fields on the header as necessary.
7. On a new line, fill in the five fields for the different permission types as described in the following table.

    |Option|Description|
    |------|-----------|
    |Blank|Specifies that the permission type is not granted for the object.|
    |**Yes**|Specifies that the permission type is granted with direct access to the object.|
    |**Indirect**|Specifies that the permission type is granted with indirect access to the object.|

    Indirect permission to a table means that you cannot open the table and read from it, but you can view the data in the table through another object, such as a page, that you have direct permission to access. For more information, see the “Example - Indirect Permission” section in this topic.

8. In the **Security Filter** field, enter a filter that you want to apply to the permission by selecting the field on which you want to limit a user's access.

    For example, if you want to create a security filter so that a user can view only sales with a specific salesperson code, you choose the field number for the **Salesperson Code** field. Then, in the **Field Filter** field, you enter the value of the that you want to use to limit access. For example, to limit a user's access to only Annette Hill's sales, enter AH.
9. Repeat steps 7 and 8 to add permissions for additional objects to the permission set.

### To create or modify permission sets by recording your actions
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Users**, and then choose the related link.
2. In the **Users** window, choose the **Permission Sets** action.
3. In the **Permission Sets** window, choose the **New** Action.
4. On a new line, fill in the fields as necessary.
5. Choose the **Permissions** action.
6. In the **Permissions** window, choose the **Start** action.

    A recording process starts to capture all your actions in the user interface.
7. Go to the various windows and activities in [!INCLUDE[d365fin](includes/d365fin_md.md)] that you want users with this permission set to access. You must carry out the tasks that you want to record permissions for.
8. When you want to finish the recording, return to the **Permissions** window, and then choose the **Stop** action.
9. Choose the **Yes** button to add the recorded permissions to the new permission set.
10. For each object in the recorded list, specify if users are able to insert, modify, or delete records in the recorded tables. See step 7 in the "To create or modify permission sets manually" section.

### Example - Indirect Permission
You can assign an indirect permission to use an object only through another object.
For example, a user can have permission to run codeunit 80, **Sales-Post**. The **Sales-Post** codeunit performs many tasks, including modifying table 37, **Sales Line**. When the user posts a sales document, the **Sales-Post** codeunit, [!INCLUDE[d365fin](includes/d365fin_md.md)] checks if the user has permission to modify the **Sales Line** table. If not, the codeunit cannot complete its tasks, and the user receives an error message. If so, the codeunit runs successfully.

However, the user does not need to have full access to the **Sales Line** table to run the codeunit. If the user has indirect permission to the **Sales Line** table, then the **Sales-Post** codeunit runs successfully. When a user has indirect permission, that user can only modify the **Sales Line** table by running the **Sales-Post** codeunit or another object that has permission to modify the **Sales Line** table. The user can only modify the **Sales Line** table when doing so from supported application areas. The user cannot run the feature inadvertently or maliciously by other methods.

## To set up user time constraints
Administrators can define periods of time during which specified users are able to post, and also specify if the system logs the amount of time users are logged on. Administrators can also assign responsibility centers to users.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Setup**, and then choose the related link.
2. In the **User Setup** window opens, choose the **New** action.
3. In the **User ID** field, enter the ID of a user, or choose the field to see all current Windows users in the system.
4. Fill in the fields as necessary.

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Getting Ready for Doing Business](ui-get-ready-business.md)  
[Setup and Administration in Dynamics NAV](admin-setup-and-administration.md)  
[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Creating Microsoft Dynamics NAV Users](/dynamics-nav/How-to--Create-Microsoft-Dynamics-NAV-Users)  
