---
title: MailMergeField.Code property (Word)
keywords: vbawd10.chm152961029
f1_keywords:
- vbawd10.chm152961029
ms.prod: word
api_name:
- Word.MailMergeField.Code
ms.assetid: 65dcf765-318b-cfc3-37e5-2a9b2a606204
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# MailMergeField.Code property (Word)

Returns a **[Range](Word.Range.md)** object that represents a field's code. Read/write.


## Syntax

_expression_. `Code`

_expression_ A variable that represents a '[MailMergeField](Word.MailMergeField.md)' object.


## Remarks

A field's code is everything that's enclosed by the field characters (**{ }**) including the leading and trailing space characters. You can access a field's code without changing the view from field results.


## Example

This example displays the field code for each field in the active document.


```vb
Dim fieldLoop As Field 
 
For Each fieldLoop In ActiveDocument.Fields 
 MsgBox Chr(34) & fieldLoop.Code.Text & Chr(34) 
Next fieldLoop
```

This example changes the field code for the first field in the active document to CREATEDATE.




```vb
Dim rngTemp As Range 
 
Set rngTemp = ActiveDocument.Fields(1).Code 
rngTemp.Text = " CREATEDATE " 
ActiveDocument.Fields(1).Update
```

This example determines whether the active document includes a mail merge field named "Title."




```vb
Dim fieldLoop As Field 
 
For Each fieldLoop In ActiveDocument.MailMerge.Fields 
 If InStr(1, fieldLoop.Code.Text, "Title", 1) Then 
 MsgBox "A Title merge field is in this document" 
 End If 
Next fieldLoop
```


## See also


[MailMergeField Object](Word.MailMergeField.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]