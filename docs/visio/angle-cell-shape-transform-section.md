---
title: Angle Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Представляет текущий угол вращения фигуры по отношению к родительскому. Формула по умолчанию для определения угла вращения фигуры 1-D: =ATAN2 (EndY-BeginY, EndX-BeginX).'
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414552"
---
# <a name="angle-cell-shape-transform-section"></a>Angle Cell (Shape Transform Section)

Представляет текущий угол вращения фигуры по отношению к родительскому. Формула по умолчанию для определения угла вращения фигуры 1-D: =ATAN2 (EndY-BeginY, EndX-BeginX).
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Angle по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Угловая  <br/> |
   
Чтобы получить ссылку на ячейку Angle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormAngle** <br/> |
   

