---
title: DisplayMode Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415819"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode Cell (Action Tags Section)

Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
|**Значение**|**Режим отображения**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Отображается, когда мышь приостанавливована на теге (по умолчанию).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1   <br/> | Отображается при выборе фигуры.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2   <br/> | Отображается постоянно.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Примечания

Теги действий не отображаются в печатных и опубликованных выходных данных. 
  
Если тег действия определен для страницы и эта ячейка содержит значение 1, тег никогда не отображается, так как страницу невозможно выбрать. 
  
Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | SmartTags.  *name*  . DisplayMode, где SmartTags. *имя* — название строки тегов действий.  <br/> |
   
Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagDisplayMode** <br/> |
   

