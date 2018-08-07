---
title: Ячейка E (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Содержит формулу неоднородной rational сплайн (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813672"
---
# <a name="e-cell-geometry-section"></a>Ячейка E (раздел "Геометрия")

Содержит формулу неоднородной rational сплайн (NURBS).
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки E по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . E *j* где *i* и *j* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки E по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j* где *j* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visNURBSData** <br/> |
   

