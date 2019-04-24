---
title: ShapePermeableX Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Определяет, может ли соединитель маршрутизироваться горизонтально через размещаемую фигуру.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357052"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>ShapePermeableX Cell (Shape Layout Section)

Определяет, может ли соединитель маршрутизироваться горизонтально через размещаемую фигуру.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включить соединители для горизонтальной маршрутизации через размещаемую фигуру.  <br/> |
|FALSE  <br/> |Не додавайте соединители маршрутизировать их горизонтально через размещаемую фигуру.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете задать значение этой ячейки на вкладке " **Размещение** " в диалоговом окне **поведение** (с выбранной фигурой на вкладке " [разработчик](run-in-developer-mode-display-the-developer-tab.md) ", в группе " **Макет фигуры** " щелкните **поведение**, а затем перейдите на вкладку **Размещение** . ). 
  
В версиях, предшествующих Visio 2000, это поведение задается с помощью ячейки Обжинтеракт в разделе Разное. 
  
Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |ShapePermeableX  <br/> |
   
Чтобы получить ссылку на ячейку ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровшапелайаут** <br/> |
|Индекс ячейки:  <br/> |**Висслопермкс** <br/> |
   

