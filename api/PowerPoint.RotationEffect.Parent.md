---
title: RotationEffect.Parent property (PowerPoint)
keywords: vbapp10.chm661002
f1_keywords:
- vbapp10.chm661002
ms.prod: powerpoint
api_name:
- PowerPoint.RotationEffect.Parent
ms.assetid: 1355565d-c2cb-2bc3-0749-c6b06efb7c25
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# RotationEffect.Parent property (PowerPoint)

Returns the parent object for the specified object.


## Syntax

_expression_.**Parent**

_expression_ A variable that represents a [RotationEffect](PowerPoint.RotationEffect.md) object.


## Return value

Object


## Example

This example adds an oval containing text to slide one in the active presentation and rotates the oval and the text 45 degrees. The parent object for the text frame is the **Shape** object that contains the text.


```vb
Set myShapes = ActivePresentation.Slides(1).Shapes

With myShapes.AddShape(Type:=msoShapeOval, Left:=50, _
        Top:=50, Width:=300, Height:=150).TextFrame

    .TextRange.Text = "Test text"
    .Parent.Rotation = 45

End With
```


## See also


[RotationEffect Object](PowerPoint.RotationEffect.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]