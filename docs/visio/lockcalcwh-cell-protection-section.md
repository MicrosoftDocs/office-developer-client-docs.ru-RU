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
description: Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при изменении вершины или при изменении типа строки в разделе Geometry.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423043"
---
# <a name="lockcalcwh-cell-protection-section"></a>LockCalcWH Cell (Protection Section)

Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при изменении вершины или при изменении типа строки в разделе Geometry.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Невозможно пересчитать ширину и высоту.  <br/> |
| FALSE  <br/> | Можно пересчитать ширину и высоту.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockCalcWH по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LockCalcWH  <br/> |
   
Чтобы получить ссылку на ячейку LockCalcWH по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровлокк** <br/> |
| Индекс ячейки:  <br/> |**вислокккалквх** <br/> |
   

