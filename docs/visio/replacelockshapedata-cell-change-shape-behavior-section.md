---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Указывает, переоформили ли значения указанных клеток в мастер-фигуре значения (в том числе локальные) фигуры, заменяемой во время операции замены фигуры. ReplaceLockShapeData определяет, переопределяют ли данные фигуры мастер-фигуры все данные фигуры, заменяемой.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408875"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>ReplaceLockShapeData Cell (Change Shape Behavior Section)

Указывает, переоформили ли значения указанных клеток в мастер-фигуре значения (в том числе локальные) фигуры, заменяемой во время операции замены фигуры. **ReplaceLockShapeData** определяет, переопределяют ли данные фигуры мастер-фигуры все данные фигуры, заменяемой. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|1 (TRUE)  <br/> |Все строки и значения раздела **Shape Data** в форме фигуры копируется в форму замены, а все локальные значения из заменяемой старой фигуры удаляются.  <br/> |
|0 (FALSE)  <br/> |Строки и значения раздела **Shape Data** в форме мастера копируется в форму замены. Любые строки в разделе **Shape Data** старой формы с локальными значениями передаются в форму замены.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ReplaceLockShapeData  <br/> |
   
Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowReplaceBehaviors** <br/> |
| Индекс ячейки:  <br/> |**visReplaceLockShapeData** <br/> |
   

