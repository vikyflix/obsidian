---
title: "Permission types (XWiki.org)"
source: "https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Access%20Rights/Permission%20types/"
author:
published:
created: 2025-11-13
description: "Permission types"
tags:
---
## Permission types

## View Right

The view right allows the user to view a document or load it using the API.

- Availability: Page, Space, and Wiki level.
- Default status: ALLOWED
- Priority order: deny > allow > no setting

## Comment Right

The comment allows the user to add a comment but not to edit or delete it.

- Availability: Page, Space, and Wiki level.
- Default status: ALLOWED
- Priority order: deny > allow > no setting

You must have edit rights on the page to edit or delete your comments. Also, you won't be able to edit or delete other users' comments, unless you have administration rights.

## Edit Right

The edit allows you to edit the page and all of its objects and attachments. Edit right implies view right.

- Availability: Page, Space and Wiki level (automatically includes the view right)
- Default status: ALLOWED
- Priority order: deny > allow > no setting

## Delete Right

The delete right allows you to move a page to the recycle bin. Delete right implies view right.

- Availability: Page, Space, and Wiki level (automatically includes the view right)
- Default status: DENIED (unless you're the document creator)
- Priority order: deny > allow > no setting

## Special Permissions

## Administration Right

The administration right can only be granted at space or wiki level. A significant detail is that a wiki or space administrator cannot have their administration rights denied for a page. This includes rights implied by admin rights. Administration rights imply the view, comment, edit, delete, and script permissions with the ability to permanently delete a page from the recycle bin. So, for example, a user with administration right on a space can always view all pages in that space regardless of other rules for the view right on the space or individual pages.

- Availability:
	- Space (Automatically includes the view, comment, edit, delete, script rights)
	- Wiki (Automatically includes the view, comment, edit, delete, script, register rights)
- Default status: DENIED
- Priority order: allow > deny > no setting

## Programming Right

A programmer is allowed to execute arbitrary Java code in the wiki, so any page saved by a user with programmer rights can run dangerous scripts. Because it affects the entire wiki (or wiki farm), programming rights can only be granted on the level of the main wiki. Like the admin right, the programming right itself and its implied rights cannot be denied.

- Availability: Main wiki level (automatically implies LOGIN, VIEW, EDIT, DELETE, REGISTER, COMMENT, SCRIPT, ADMIN, see the documentation for the [security module](https://extensions.xwiki.org/xwiki/bin/view/Extension/Security%20Module))
- Default status: DENIED
- Priority order: allow > deny > no setting

The register right is usually granted or revoked for the non-registered pseudo-user "XWiki.XWikiGuest". This permission can only be set from the wiki preferences page.

- Availability: Wiki level
- Default status: ALLOWED
- Priority order: allow > deny > no setting

## Create Wikis Right

The "create wiki" right can only be granted via the main wiki, just like programming rights.

- Availability: Main wiki level
- Default status: DENIED
- Priority order: allow > deny > no setting

## Script Right

The "Script" right was introduced in version 7.2 to control who has the right to write scripts. Anyone with edit rights can write a script on a wiki page. However, when the page is rendered, the script will only execute if the last author of the page has the "Script" right.

XWiki <14.10

For backwards-compatibility reasons, the standard XWiki distribution comes with the "Script" right being allowed for all users at the main wiki level. So, unless an administrator explicitly revokes the right for some users or groups, they can execute the scripts they wrote.

XWiki 14.10+

The script right gives a lot of power to users, so by default, the right is not given anymore to all users at the main wiki level: administrators have to allow it manually.

- Availability: Page, Space and Wiki level.
- Default status: DENIED
- Priority order: deny > allow > no setting

## Tabular view

| Right | Description | Default | Priority <sup xmlns="http://www.w3.org/1999/xhtml">1)</sup> | Targeted entities | Remarks |
| --- | --- | --- | --- | --- | --- |
| **View** | The view right allows the user to view a document or load it using the API. | Allow | deny >   allow >   no setting | Wiki, Space, Document |  |
| **Comment** | The comment allows the user to add a comment, but not to edit or delete it. | Allow | deny >   allow >   no setting | Wiki, Space, Document | You must have edit rights on the page to edit or delete your comments. Also, you won't be able to edit or delete other users' comments unless you have administration rights. |
| **Edit** | The edit allows you to edit the page and all of its objects. | Allow | deny >   allow >   no setting | Wiki, Space, Document | Automatically includes the view right |
| **Delete** | The delete right allows you to move a page to the recycle bin. | Deny | deny >   allow >   no setting | Wiki, Space, Document | Automatically includes the view right |
| **Administration** | The administration right can only be granted at space or wiki level. A significant detail is that a wiki or space administrator cannot have their administration rights denied for a page. Also, administration rights imply the view, comment, edit, delete, and script permissions with the ability to permanently delete a page from the recycle bin. | Deny | allow >   deny >   no setting | Wiki, Space |  |
| **Programming** | A programmer is allowed to execute arbitrary Java code in the wiki, so any page saved by a user with programmer rights can run dangerous scripts. Because it affects the entire wiki (or wiki farm), programming rights can only be granted from the wiki preferences page in a single wiki environment or from the main wiki in a multi-wiki environment. | Deny | allow >   deny >   no setting | Main wiki | Main wiki level (automatically implies LOGIN, VIEW, EDIT, DELETE, REGISTER, COMMENT, SCRIPT, ADMIN, see the documentation for the [security module](https://extensions.xwiki.org/xwiki/bin/view/Extension/Security%20Module)) |
| **Register** | The register right is usually granted or revoked for the non-registered pseudo-user "XWiki.XWikiGuest". This permission can only be set from the wiki preferences page. | Allow | allow >   deny >   no setting | Wiki | Wiki level only |
| **Create Wikis** | The "create wiki" right can only be granted via the main wiki, just like programming rights | Deny | allow >   deny >   no setting | Main wiki only | Main wiki level only |
| **Script** | The "Script" right was introduced in version 7.2 to control who has the right to write scripts. Anyone with edit rights can write a script on a wiki page. However, when the page is rendered, the script will only execute if the last author of the page has the "Script" right. | XWiki <14.10 Allow XWiki 14.10+ Deny (Main Wiki)  Deny (Sub Wiki) | deny >   allow >   no setting | Wiki, Space, Document | XWiki <14.10  For backwards-compatibility reasons, the standard XWiki distribution comes with the "Script" right being allowed for all users at the main wiki level. So, unless an administrator explicitly revokes the right for some users or groups, they can execute the scripts they wrote.  XWiki 14.10+  The script right gives a lot of power to users, so by default, the right is not given anymore to all users at the main wiki level: administrators have to allow it manually. |

<sup>1)</sup> For “deny > allow”, any encounter of an explicit deny will deny the permission  
For “allow > deny”, allow right will overrule any implicit or explicit deny

[Another table with additional information about implied rights, inheritance and more](https://extensions.xwiki.org/xwiki/bin/view/Extension/Security%20Module#HDefaultrightsbeingpredefined).

- Today
- Yesterday
- Last 7 days
- Last 30 days
- This month
- Last month
- Custom Range