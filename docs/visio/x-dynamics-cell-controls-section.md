---
title: X Dynamics ячейки (раздел элементы управления)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Представляет x-координаты точки привязки управляющего маркера в локальной системе координат.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815211"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics ячейки (раздел элементы управления)

Представляет *x* -координаты точки привязки управляющего маркера в локальной системе координат. 
  
## <a name="remarks"></a>Замечания

Точка привязки используется для эластичное во время dynamics.
  
Для получения ссылки на ячейки X Dynamics по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Элементы управления.  *имя* . Элементы управления XDynwhere.  *имя* — это имя строки элементов управления.  <br/> |
   
Для получения ссылки на ячейки X Dynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCtlXDyn** <br/> |
   

