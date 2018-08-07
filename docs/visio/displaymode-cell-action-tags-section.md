---
title: Ячейка DisplayMode (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Определяет, отображается ли тег действия при наведении указателя мыши на тег, при выборе фигуры или все время.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813596"
---
# <a name="displaymode-cell-action-tags-section"></a>Ячейка DisplayMode (раздел "Теги действий")

Определяет, отображается ли тег действия при наведении указателя мыши на тег, при выборе фигуры или все время.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Режим отображения**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Отображается при наведении курсора на тег (по умолчанию).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Появляется при выбранной фигуре.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Появляется при запуске.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Замечания

Теги действий не отображаются на печати и опубликованные выходные данные. 
  
Если тег действие определенные на странице, и эта ячейка содержит значение 1, тега никогда не отображается, поскольку страница не может быть выбран. 
  
Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . DisplayMode где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки DisplayMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagDisplayMode** <br/> |
   

