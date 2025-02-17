---
title: Form.WindowTop property (Access)
keywords: vbaac10.chm13516
f1_keywords:
- vbaac10.chm13516
ms.prod: access
api_name:
- Access.Form.WindowTop
ms.assetid: 1257fe21-3983-bd51-4683-e0778b59a975
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Form.WindowTop property (Access)

Returns an **Integer** indicating the screen position in [twips](../language/glossary/vbe-glossary.md#twip) of the top edge of a form relative to the top of the Microsoft Access window. Read-only.


## Syntax

_expression_.**WindowTop**

_expression_ A variable that represents a **[Form](Access.Form.md)** object.


## Remarks

Use the **Move** method to change the position of a form.


## Example

The following example returns the screen position of the top and left edges of the first form in the current project.

```vb
With Forms(0) 
 
 MsgBox "The form is " & .WindowLeft _ 
 & " twips from the left edge of the Access window and " _ 
 & .WindowTop _ 
 & " twips from the top edge of the Access window." 
 
End With 

```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]