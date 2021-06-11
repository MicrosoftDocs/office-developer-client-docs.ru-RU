---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Указывает список ячеек в shapeSheet, которые копируется из старой формы в форму замены во время операции замены фигуры.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409344"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>ReplaceCopyCells Cell (Change Shape Behavior Section)

Указывает список ячеек в shapeSheet, которые копируется из старой формы в форму замены во время операции замены фигуры. 
  
## <a name="remarks"></a>Примечания

В магистрали замены должен содержаться вызов **функции DEPENDSON** в ячейке **ReplaceCopyCells,** где каждый аргумент в функции является ссылкой на ячейку. Эти ячейки копируется из старой формы в форму, которая является результатом операции замены фигуры, независимо от того, где они находятся в ShapeSheet. 
  
Значения и/или формулы, ссылаясь на другие ячейки, копируется в фигуру. Если в фигуре не имеется ссылочная ячейка, скопированная ячейка содержит только значение. 
  
Ссылки в **ячейке ReplaceCopyCells** переопределяют защиту, установленную на ячейках, как определено в разделе Защита и **ReplaceLockFormat,** **ReplaceLockShapeData** и **ReplaceLockText** ячейки.  
  
Чтобы получить ссылку на ячейку **ReplaceCopyCells** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ReplaceCopyCells  <br/> |
   
Чтобы получить ссылку на ячейку **ReplaceCopyCells** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowReplaceBehaviors** <br/> |
| Индекс ячейки:  <br/> |**visReplaceCopyCells** <br/> |
   

