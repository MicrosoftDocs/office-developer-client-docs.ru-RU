---
title: FlipX Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Указывает, была ли фигура перевернута по горизонтали.
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415952"
---
# <a name="flipx-cell-shape-transform-section"></a>FlipX Cell (Shape Transform Section)

Указывает, была ли фигура перевернута по горизонтали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура была перевернута по горизонтали.  <br/> |
| FALSE  <br/> | Фигура не была перевернута по горизонтали.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку FlipX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | FlipX  <br/> |
   
Чтобы получить ссылку на ячейку FlipX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormFlipX** <br/> |
   

