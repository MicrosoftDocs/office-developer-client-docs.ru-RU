---
title: Ячейка X Dynamics (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Представляет x-координату для точки привязки управляющего маркера в локальных координатах.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815211"
---
# <a name="x-dynamics-cell-controls-section"></a>Ячейка X Dynamics (раздел "Элементы управления")

Представляет *x*-координату для точки привязки управляющего маркера в локальных координатах. 
  
## <a name="remarks"></a>Замечания

Точка привязки используется для эластичного соединения при движении.
  
Чтобы получить ссылку на ячейку X Dynamics по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Controls.  *имя* .XDyn, где Controls.  *имя* — название строки элементов управления.  <br/> |
   
Чтобы получить ссылку на ячейку X Dynamics по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visCtlXDyn** <br/> |
   

