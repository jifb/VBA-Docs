---
title: Section.OnPrint property (Access)
keywords: vbaac10.chm12205
f1_keywords:
- vbaac10.chm12205
ms.prod: access
api_name:
- Access.Section.OnPrint
ms.assetid: f8df36f2-697b-7a1d-6343-76d2a2a7b0cf
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# Section.OnPrint property (Access)

Sets or returns the value of the **On Print** box in the Properties window of a report section. Read/write **String**.


## Syntax

_expression_.**OnPrint**

_expression_ A variable that represents a **[Section](Access.Section.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The **Print** event occurs after data in a report section is formatted for printing, but before the section is printed.

The **OnPrint** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Print** box in the report section's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Print** box is blank, the property value is an empty string.


## Example

The following example prints the value of the **OnPrint** property in the Immediate window for the "GroupHeader0" section in the **Purchase Order** report.

```vb
Debug.Print Reports("Purchase Order").Section("GroupHeader0").OnPrint
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]