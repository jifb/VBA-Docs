---
title: Attachment.MouseMove event (Access)
keywords: vbaac10.chm14030
f1_keywords:
- vbaac10.chm14030
ms.prod: access
api_name:
- Access.Attachment.MouseMove
ms.assetid: 61ec0bdb-6e39-a4a7-92aa-45d543e35109
ms.date: 02/07/2019
ms.localizationpriority: medium
---


# Attachment.MouseMove event (Access)

The **MouseMove** event occurs when the user moves the mouse.


## Syntax

_expression_.**MouseMove** (_Button_, _Shift_, _X_, _Y_)

_expression_ A variable that represents an **[Attachment](Access.Attachment.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Button_|Required|**Integer**|The button that was pressed or released when the event was triggered. If you need to test for the _Button_ argument, you can use one of the following intrinsic constants as bit masks:<ul><li><p><b>acLeftButton</b>  The bit mask for the left mouse button.</p></li><li><p><b>acRightButton</b>  The bit mask for the right mouse button.</p></li><li><p><b>acMiddleButton</b>  The bit mask for the middle mouse button.</p></li></ul> |
| _Shift_|Required|**Integer**|The state of the Shift, Ctrl, and Alt keys when the button specified by the _Button_ argument was pressed or released. If you need to test for the _Shift_ argument, you can use one of the following intrinsic constants as bit masks:<ul><li><p><b>acShiftMask</b>  The bit mask for the Shift key.</p></li><li><p><b>acCtrlMask</b>  The bit mask for the Ctrl key.</p></li><li><p><b>acAltMask</b>  The bit mask for the Alt key.</p></li></ul>|  
| _X_|Required|**Single**|The _x_ coordinate for the current location of the mouse pointer, in [twips](../language/glossary/vbe-glossary.md#twip). |
| _Y_|Required|**Single**|The _y_ coordinate for the current location of the mouse pointer, in twips. |


## Remarks

The **MouseMove** event applies only to forms, form sections, and controls on a form, and not to controls on a report.
    
This event does not apply to a label attached to another control, such as the label for a text box. It applies only to "freestanding" labels. Pressing and releasing a mouse button in an attached label has the same effect as pressing and releasing the button in the associated control. The normal events for the control occur; no separate events occur for the attached label.

To run a macro or event procedure when these events occur, set the **OnMouseMove** property to the name of the macro or to [Event Procedure].

The **MouseMove** event is generated continually as the mouse pointer moves over objects. Unless another object generates a mouse event, an object recognizes a **MouseMove** event whenever the mouse pointer is positioned within its borders.

To cause a **MouseMove** event for a form to occur, move the mouse pointer over a blank area, record selector, or scroll bar on the form. To cause a **MouseMove** event for a form section to occur, move the mouse pointer over a blank area of the form section.

To respond to an event caused by moving the mouse, you use a **MouseMove** event.

To run a macro or event procedure in response to pressing and releasing the mouse buttons, you use the **MouseDown** and **MouseUp** events.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]