---
title: Ячейка Angle (раздел "Преобразование фигур")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Представляет фигуры текущий угол вращения относительно его родительского элемента. Формула по умолчанию для угла фигуры 1 D: = ATAN2(EndY-BeginY,EndX-BeginX).'
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813145"
---
# <a name="angle-cell-shape-transform-section"></a>Ячейка Angle (раздел "Преобразование фигур")

Представляет фигуры текущий угол вращения относительно его родительского элемента. Формула по умолчанию для угла фигуры 1 D: = ATAN2(EndY-BeginY,EndX-BeginX).
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки угол по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Угол  <br/> |
   
Для получения ссылки на ячейки угол по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormAngle** <br/> |
   

