---
title: Ячейка Y Justify (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Смещение по оси Y для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357017"
---
# <a name="y-justify-cell-action-tags-section"></a>Ячейка Y Justify (раздел "Теги действий")

Смещение по оси *y* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Выравнивание по верхнему краю (по умолчанию).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1,1  <br/> | Выравнивание по центру.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | Выравнивание по нижнему краю.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Замечания

Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y.
  
Чтобы получить ссылку на ячейку Y Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *имя* .YJustify, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку Y Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagYJustify** <br/> |
   

