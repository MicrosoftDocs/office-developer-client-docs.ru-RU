---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. ReplaceLockShapeData определяет, переопределяются ли все данные фигуры заменяемой фигуры.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408875"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>ReplaceLockShapeData Cell (Change Shape Behavior Section)

Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. **ReplaceLockShapeData** определяет, переопределяются ли все данные фигуры заменяемой фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|1 (TRUE)  <br/> |Все строки и значения раздела **"Данные** фигуры" фигуры копируется на заменяемую фигуру, а все локальные значения из заменяемой старой фигуры удаляются.  <br/> |
|0 (FALSE)  <br/> |Строки и значения раздела **"Данные** фигуры" фигуры копируется в заменяемую фигуру. Все строки в разделе **"Данные фигуры"** старой фигуры с локальными значениями переносятся на заменяемую фигуру.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ReplaceLockShapeData  <br/> |
   
Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowReplaceBehaviors** <br/> |
| Индекс ячейки:  <br/> |**visReplaceLockShapeData** <br/> |
   

