---
title: Width Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Содержит ширину выбранной фигуры в единицах рисования. Формула по умолчанию для определения ширины 1-D фигуры:'
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415196"
---
# <a name="width-cell-shape-transform-section"></a>Width Cell (Shape Transform Section)

Содержит ширину выбранной фигуры в единицах рисования. Формула по умолчанию для определения ширины 1-D фигуры:
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - Beginy) ^ 2)
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Width по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Width  <br/> |
   
Чтобы получить ссылку на ячейку Width по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormWidth** <br/> |
   

