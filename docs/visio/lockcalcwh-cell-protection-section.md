---
title: LockCalcWH Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Блокирует прямоугольник выбора фигуры, поэтому его невозможно пересчитать при редактировании вершины или изменения типа строки в разделе Геометрия.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423043"
---
# <a name="lockcalcwh-cell-protection-section"></a>LockCalcWH Cell (Protection Section)

Блокирует прямоугольник выбора фигуры, поэтому его невозможно пересчитать при редактировании вершины или изменения типа строки в разделе Геометрия.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Ширина и высота не могут быть пересчитаны.  <br/> |
| FALSE  <br/> | Ширина и высота можно пересчитать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockCalcWH  <br/> |
   
Чтобы получить ссылку на ячейку LockCalcWH по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLock** <br/> |
| Индекс ячейки:  <br/> |**visLockCalcWH** <br/> |
   

