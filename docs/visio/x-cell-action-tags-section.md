---
title: Ячейка X (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Положение на оси x в локальных координатах фигуры, относительно которого размещается кнопка тега действия.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431115"
---
# <a name="x-cell-action-tags-section"></a>Ячейка X (раздел "Теги действий")

Положение на оси *x* в локальных координатах фигуры, относительно которого размещается кнопка тега действия. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Ячейки X и Y определяют точку в локальных координатах фигуры, а ячейки X Justify и Y Justify определяют, где должна быть размещена кнопка тега действия относительно этой точки. 
  
Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> |SmartTags. *имя* .X, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagX** <br/> |
   

