---
title: Y выровнять ячейки (действие помечает раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Y — смещение кнопки тега действия относительно точки, заданной ячейками X и Y.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815219"
---
# <a name="y-justify-cell-action-tags-section"></a>Y выровнять ячейки (действие помечает раздел)

*Y* — смещение кнопки тега действия относительно точки, заданной ячейками X и Y. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По верхнему краю (по умолчанию).  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | По центру.  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | По нижнему краю.  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>Замечания

Выровнять X и Y ширине ячеек определить размещение кнопки тега действия при использовании точки, заданной в ячейках X и Y.
  
Для получения ссылки на ячейки ширине Y по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . YJustify где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки ширине Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagYJustify** <br/> |
   

