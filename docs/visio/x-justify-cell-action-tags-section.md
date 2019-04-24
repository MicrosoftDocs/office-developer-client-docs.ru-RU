---
title: Ячейка X Justify (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Смещение по оси x для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284974"
---
# <a name="x-justify-cell-action-tags-section"></a>Ячейка X Justify (раздел "Теги действий")

Смещение по оси *x* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Выравнивание по левому краю (по умолчанию).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1,1  <br/> | Выравнивание по центру.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | Выравнивание по правому краю.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Замечания

Ячейки X Justify и Y Justify указывают, где размещается кнопка тега действия по отношению к точке, определенной в ячейках X и Y. 
  
Чтобы получить ссылку на ячейку X Justify по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *имя* .XJustify, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку X Justify по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagXJustify** <br/> |
   

