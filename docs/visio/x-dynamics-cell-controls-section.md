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
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322304"
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
   

