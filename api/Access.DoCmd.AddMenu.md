---
title: DoCmd.AddMenu method (Access)
keywords: vbaac10.chm4141
f1_keywords:
- vbaac10.chm4141
ms.prod: access
api_name:
- Access.DoCmd.AddMenu
ms.assetid: d2db2143-fd15-56b3-ee99-b895bc6b21f8
ms.date: 03/06/2019
ms.localizationpriority: medium
---


# DoCmd.AddMenu method (Access)

The **AddMenu** method carries out the AddMenu action in Visual Basic.


## Syntax

_expression_.**AddMenu** (_MenuName_, _MenuMacroName_, _StatusBarText_)

_expression_ A variable that represents a **[DoCmd](Access.DoCmd.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _MenuName_|Required|**Variant**|A string expression that's the valid name of a drop-down menu to add to the custom menu bar or global menu bar. To create an access key so that you can use the keyboard to choose the menu, type an ampersand (&) before the letter you want to be the access key. This letter will be underlined in the menu name on the menu bar.|
| _MenuMacroName_|Required|**Variant**|A string expression that's the valid name of the macro group that contains the macros for the menu's commands. This is a required argument.|
| _StatusBarText_|Required|**Variant**|A string expression that's the text to display in the status bar when the menu is selected.|

## Remarks

Use the AddMenu action to create a:

- **Custom menu bar** for a form or report. The custom menu bar replaces the built-in menu bar for the form or report.
    
- **Custom shortcut menu** for a form, form control, or report. The custom shortcut menu replaces the built-in shortcut menu for the form, form control, or report.
    
- **Global menu bar**. The global menu bar replaces the built-in menu bar for all Microsoft Access windows, except where you've added a custom menu bar for a form or report.
    
- **Global shortcut menu**. The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms in Form view, Datasheet view, and Print Preview, and reports in Print Preview, except where you've added a custom shortcut menu for a form, form control, or report.
    
You must include the _MenuName_ and _MenuMacroName_ arguments in the **AddMenu** method for custom menu bars and global menu bars. The _MenuName_ argument is not required and will be ignored for custom shortcut menus and global shortcut menus.

The _StatusBarText_ argument is optional; this argument is ignored for custom shortcut menus and global shortcut menus.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]