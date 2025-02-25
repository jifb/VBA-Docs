---
title: Borders object (Excel)
keywords: vbaxl10.chm180072
f1_keywords:
- vbaxl10.chm180072
ms.prod: excel
api_name:
- Excel.Borders
ms.assetid: adb6efd6-73b6-e620-e9be-f4a42bc52ae8
ms.date: 03/29/2019
ms.localizationpriority: medium
---


# Borders object (Excel)

A collection of four **[Border](Excel.Border(object).md)** objects that represent the four borders of a **[Range](Excel.Range(object).md)**  object or **[Style](Excel.Style.md)** object.


## Remarks

Use the **Borders** property to return the **Borders** collection, which contains all four borders. You can apply different borders to each side of a cell or range. For more information how to apply borders to a range of cells, see **[Range.Borders](Excel.Range.Borders.md)** property.

You can set border properties for an individual border only with **Range** and **Style** objects. Other bordered objects, such as error bars and series lines, have a border that's treated as a single entity, regardless of how many sides it has. For these objects, you must return and set properties for the entire border as a unit. For more information, see the **Border** object.


## Examples

The following example adds a double border to cell A1 on worksheet one.

```vb
Worksheets(1).Range("A1").Borders.LineStyle = xlDouble
```

The following example adds a double border on the inside as well as outside to a range selection from A1 to C3 on worksheet one.

```vb
Worksheets(1).Range("A1:C3").Borders.LineStyle = xlDouble
```

Use **Borders** (_index_), where _index_ identifies the border, to return a single **Border** object. _Index_ can be one of the following **[XlBordersIndex](Excel.XlBordersIndex.md)** constants: **xlDiagonalDown**, **xlDiagonalUp**, **xlEdgeBottom**, **xlEdgeLeft**, **xlEdgeRight**, **xlEdgeTop**, **xlInsideHorizontal**, or **xlInsideVertical**.

The following example sets the color of the bottom border of cells A1:G1 to red.

```vb
Worksheets("Sheet1").Range("A1:G1"). _ 
 Borders(xlEdgeBottom).Color = RGB(255, 0, 0)
```
The following example generates a thin border around all cells in the range.

```vb
Dim rng As Range: Set rng = ws.Range("B6", "D8")
        
With rng.Borders
   .LineStyle = xlContinuous
   .Weight = xlThin
End With
```

The following example changes only the inner cell borders of the range. 

```vb
Dim rngInner As Range: Set rngInner = ws.Range("B2", "D4")
        
With rngInner.Borders(xlInsideHorizontal)
  .LineStyle = xlContinuous
  .Weight = xlThin
End With

With rngInner.Borders(xlInsideVertical)
  .LineStyle = xlContinuous
  .Weight = xlThin
End With
```

## Properties

- [Application](Excel.Borders.Application.md)
- [Color](Excel.Borders.Color.md)
- [ColorIndex](Excel.Borders.ColorIndex.md)
- [Count](Excel.Borders.Count.md)
- [Creator](Excel.Borders.Creator.md)
- [Item](Excel.Borders.Item.md)
- [LineStyle](Excel.Borders.LineStyle.md)
- [Parent](Excel.Borders.Parent.md)
- [ThemeColor](Excel.Borders.ThemeColor.md)
- [TintAndShade](Excel.Borders.TintAndShade.md)
- [Value](Excel.Borders.Value.md)
- [Weight](Excel.Borders.Weight.md)

## See also

- [Excel Object Model Reference](overview/Excel/object-model.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
