---
title: Ячейка Y Dynamics (раздел элементы управления)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Представляет y-координаты точки привязки управляющего маркера в локальной системе координат. Точка привязки используется для эластичное во время dynamics.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815241"
---
# <a name="y-dynamics-cell-controls-section"></a>Ячейка Y Dynamics (раздел элементы управления)

Представляет *y* -координаты точки привязки управляющего маркера в локальной системе координат. Точка привязки используется для эластичное во время dynamics. 
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки Y Dynamics по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Элементы управления.  *имя* . Элементы управления YDynwhere.  *имя* — это имя строки элементов управления.  <br/> |
   
Для получения ссылки на ячейки Y Dynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visCtlYDyn** <br/> |
   

