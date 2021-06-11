---
title: ShdwObliqueAngle Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Содержит номер, указывающий угол наклонного направления при применении теневого типа страницы по умолчанию.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430429"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>ShdwObliqueAngle Cell (Page Properties Section)

Содержит номер, указывающий угол наклонного направления при применении теневого типа страницы по умолчанию.
  
## <a name="remarks"></a>Примечания

Значение 0 (0) в этой ячейке указывает, что направление угла прямо вверх и измеряется перемещением по часовой стрелке.
  
 Угол, описанный в этой ячейке, используется всякий раз, когда ячейка ShapeShdwType (тип тени для фигуры на странице) задает значение Page Default **(visFSTPageDefault),** а тип тени косый. Тип теней страницы по умолчанию определяется в ячейке ShdwType. 
  
Чтобы настроить это поведение для отдельной фигуры, используйте ячейку ShapeShdwObliqueAngle в разделе Формат заполнения.
  
Чтобы получить ссылку на ячейку ShdwObliqueAngle по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ShdwObliqueAngle  <br/> |
   
Чтобы получить ссылку на ячейку ShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

