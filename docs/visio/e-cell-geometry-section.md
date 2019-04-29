---
title: E Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Содержит формулу неоднородного рационального B-сплайна (NURBS).
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423568"
---
# <a name="e-cell-geometry-section"></a>E Cell (Geometry Section)

Содержит формулу неоднородного рационального B-сплайна (NURBS).
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку E по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Геометрия *i* . E *j* , где *i* и *j* = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку E по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowVertex** +  *j*, где *j* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**Виснурбсдата** <br/> |
   

