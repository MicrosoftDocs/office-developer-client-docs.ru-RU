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
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404829"
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
   

