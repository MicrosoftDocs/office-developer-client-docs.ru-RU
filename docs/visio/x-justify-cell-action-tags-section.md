---
title: X ширине ячейки (раздел теги действие)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: X - смещение кнопки тега действия относительно точки, заданной ячейками X и Y.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815189"
---
# <a name="x-justify-cell-action-tags-section"></a>X ширине ячейки (раздел теги действие)

*X* -смещение кнопки тега действия относительно точки, заданной ячейками X и Y. 
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов. 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По левому краю (по умолчанию).  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | По центру.  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | По правому краю.  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>Замечания

Выровнять X и Y ширине ячеек определить размещение кнопки тега действия при использовании точки, заданной в ячейках X и Y. 
  
Для получения ссылки на ячейку обоснование X по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Смарт-тегов.  *имя* . XJustify где смарт-тегов. *имя* — это имя строки тега действия  <br/> |
   
Для получения ссылки на ячейки обоснование X по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionSmartTag** <br/> |
| Индекс строки:  <br/> |**visRowSmartTag** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSmartTagXJustify** <br/> |
   

