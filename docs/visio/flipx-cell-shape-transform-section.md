---
title: Ячейка FlipX (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Указывает, является ли фигура отразилось по горизонтали.
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813789"
---
# <a name="flipx-cell-shape-transform-section"></a>Ячейка FlipX (раздел "Преобразование фигуры")

Указывает, является ли фигура отразилось по горизонтали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | По горизонтали отразилось фигуры.  <br/> |
| FALSE  <br/> | Фигура не отразилось по горизонтали.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку FlipX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | FlipX  <br/> |
   
Для получения ссылки на ячейки FlipX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormFlipX** <br/> |
   

