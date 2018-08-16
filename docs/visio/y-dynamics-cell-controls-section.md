---
title: Ячейка Y Dynamics (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Представляет y-координату для точки привязки управляющего маркера в локальных координатах. Точка привязки используется для эластичного соединения при движении.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815241"
---
# <a name="y-dynamics-cell-controls-section"></a>Ячейка Y Dynamics (раздел "Элементы управления")

Представляет *y*-координату для точки привязки управляющего маркера в локальных координатах. Точка привязки используется для эластичного соединения при движении. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку Y Dynamics по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Controls.  *имя* .YDyn, где Controls.  *имя* — название строки элементов управления.  <br/> |
   
Чтобы получить ссылку на ячейку Y Dynamics по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visCtlYDyn** <br/> |
   

