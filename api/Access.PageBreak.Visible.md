---
title: PageBreak.Visible property (Access)
keywords: vbaac10.chm11678
f1_keywords:
- vbaac10.chm11678
ms.prod: access
api_name:
- Access.PageBreak.Visible
ms.assetid: bce10ac3-a7a5-5d0e-df76-b8222aa64267
ms.date: 02/27/2019
ms.localizationpriority: medium
---


# PageBreak.Visible property (Access)

Returns or sets whether the object is visible. Read/write **Boolean**.


## Syntax

_expression_.**Visible**

_expression_ A variable that represents a **[PageBreak](Access.PageBreak.md)** object.


## Remarks

To hide an object when printing, use the **DisplayWhen** property.

Use the **Visible** property to hide a control on a form or report by including the property in a macro or event procedure that runs when the **Current** event occurs. For example, you can show or hide a congratulatory message next to a salesperson's monthly sales total in a sales report, depending on the sales total.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]