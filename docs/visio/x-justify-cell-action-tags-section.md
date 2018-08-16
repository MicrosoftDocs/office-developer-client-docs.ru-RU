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
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815189"
---
# <a name="x-justify-cell-action-tags-section"></a>Ячейка X Justify (раздел "Теги действий")

Смещение по оси *x* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Выравнивание по левому краю (по умолчанию).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | Выравнивание по центру.  <br/> |**visSmartTagXJustifyCenter** <br/> |
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
   

