---
title: ShapeRange.IsInline property (Publisher)
keywords: vbapb10.chm2294022
f1_keywords:
- vbapb10.chm2294022
ms.prod: publisher
api_name:
- Publisher.ShapeRange.IsInline
ms.assetid: 32e038cc-5837-93b4-de54-9bcd0549f1d4
ms.date: 06/14/2019
ms.localizationpriority: medium
---


# ShapeRange.IsInline property (Publisher)

Returns an **[MsoTriState](office.msotristate.md)** constant that specifies whether a shape is inline. Read-only.


## Syntax

_expression_.**IsInline**

_expression_ A variable that represents a **[ShapeRange](Publisher.ShapeRange.md)** object.


## Example

This example tests the first shape (a text frame) on the first page of the publication to see if it is inline. If it is not, a search is done within that shape to find any inline shapes within the text frame. Any inline shapes that are found have the **ForeColor** property set to red.

```vb
Dim theShape As Shape 
Dim i As Integer 
 
Set theShape = ActiveDocument.Pages(1).Shapes(1) 
 
If Not theShape.IsInline = True Then 
 With theShape.TextFrame.Story.TextRange 
 If .InlineShapes.Count > 0 Then 
 For i = 1 To .InlineShapes.Count 
 .InlineShapes(i).Select 
 .InlineShapes(i).Fill.ForeColor.RGB = vbRed 
 Next 
 End If 
 End With 
End If
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]