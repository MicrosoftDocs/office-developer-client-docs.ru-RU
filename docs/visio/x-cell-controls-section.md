---
title: Ячейка X (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Представляет x-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406453"
---
# <a name="x-cell-controls-section"></a>Ячейка X (раздел "Элементы управления")

Представляет *x*-координату, определяющую расположение управляющего маркера фигуры в локальных координатах. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Controls.  *имя* .X, где Controls.  *имя* — название строки элементов управления.  <br/> |
   
Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visCtlX** <br/> |
   

